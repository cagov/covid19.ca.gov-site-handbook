---
title: Fully accessible dashboards 
date: 2021-01-15
permalink: /tech/fast-dashboards/
toc: true
eleventyNavigation:
  key: Fully accessible dashboards 
  order: 48 
  parent: Tech
---

We set goals for our dashboards in the areas of:

* Accessibility
* Performance
* Reliability
* Maintenance

[California’s commitment to health equity](https://covid19.ca.gov/equity/) is an example of a dashboard that meets our goals. We evaluated several charting tools to find one that helped us to meet our goals. We used D3.js for all the data visualizations on this dashboard.

## Why

The biggest wins using D3 were:

* __Raw performance__: The total weight of the code behind the equity dashboard is < 1% the size of the Tableau code we used on the [state dashboard](https://covid19.ca.gov/state-dashboard/). The rendering time for D3 is very fast compared to Tableau. Here’s a side by side comparison: 
<iframe width="560" height="315" src="https://www.youtube.com/embed/xki_Jo0NlM4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

* __We exceeded our accessibility standards__: The charts on the equity elements can be tabbed through so they can be used effectively with a screenreader. Dashboards built with tools like Tableau often do not make the visualization itself accessible. Instead they meet legal accessibility requirements with a short text summary outside the data visualization.
* __Complete translations__: D3 allowed us to translate the whole chart, down to the tooltips and labels. This deep translation integration was too difficult to do in dashboards built with other tools.

These are huge upgrades for the end user. Performance, accessibility, or translation failures may make a dashboard unusable for some Californians.

Other benefits of D3 architecture compared to the other tools currently used by state dev teams include:

* Data updates happen completely independently of visual representation code. 
* Chart data visualization code is part of the existing front end codebase. This means:
  * It requires no additional external services or subscriptions and introduces no new possible points of failure.
  * It inherits all existing environment integrations. This lets the code pull from data sets to be reviewed in staging and fully-vetted datasets in production using existing build system variables.
  * The chart visualization code is javascript and CSS. This lets any web developer troubleshoot or modify it without new tools or licenses.
  * The chart visualization code is checked into the same git repository as the rest of the site. Changes are tracked and standard rollback procedures are available.
  * Any desired layout changes happen with the existing publishing workflow. This means existing automated test tools run against the page and chart updates.
* We embed each chart into its own web component. This encapsulates the execution environment into its own class. It can be tested, modified in isolation, or quickly removed by dropping the import statement and custom element.

## How

We use the D3.js javascript library to output svg charts. We encapsulate each chart’s unique code in a web component. 

### Web components

We use web components to wrap each of our charts in a separate javascript class. Web components are not required for chart development. Web components are the browser’s built in method of creating custom user interface elements. Web components allow you to define your own HTML tags known as custom elements. You associate your own javascript class with the custom element and the browser will execute a set of events associated with each custom element discovered in markup.

Here’s an example of a custom element:

```<cagov-equity-bar-chart data-url=”https://files.covid19.ca.gov/data/reviewed/equity/social-income.json” />```

The chart data source is passed in as a custom element data attribute and the data URL is defined with environment specific build time logic. All the chart code is inside our component class. It receives a set of component-specific lifecycle events and has access to standard DOM element functions.

Google offers more info on [web components](https://developers.google.com/web/updates/2017/01/webcomponents-org?hl=en).

### D3

There are many similar open source charting libraries. The state has shipped sites using highcharts, there are tons of other lightweight charting tools like chart.js and Frappe. 

We chose D3 because it:

* Is open source
* Requires no license to use
* Has a large feature set for its small code footprint
* Has good documentation
* Has a strong community built over years that shares a lot of code and data visualization examples

Most of the js library type charting tools have similar basic feature sets and total code size measured in KB. These charts render much faster for end users than tools like Tableau. While Tableau allows you to drag and drop to create data visualizations, they end up outputting code sizes for users measured in MB.

D3 is often found on sites the Office of the Governor refers to as good examples of dashboards. One leading example is the [LA Times COVID-19 dashboard](https://www.latimes.com/projects/california-coronavirus-cases-tracking-outbreak/). Mapbox also uses D3 for [presenting regional data](https://blog.mapbox.com/how-we-built-usa-todays-election-night-maps-33b8a4b246b1).

#### Intro to D3

A good place to start is the [D3 API reference](https://github.com/d3/d3/blob/master/API.md).

[Observable](https://observablehq.com/) is useful for prototyping because:

* It has a friendly interface where you immediately see the results of code changes
* Anyone can start a data visualization without having to do any local environment scaffolding

It’s also easy to:

* Find prior examples to fork and modify
* Importing data files or external libraries
* Use the sharing feature to send working versions back and forth with anyone

Examples of basic chart functions

* [Bar chart with the background color filled in](https://observablehq.com/@aaronhans/test-background-fill)
* [California map with county boundaries and tooltips](https://observablehq.com/@aaronhans/ca-county-tiers)

Full tutorials

* [Official D3 tutorial from the D3 maintainers](https://observablehq.com/@d3/learn-d3)
* [Nice D3 tutorial walkthrough from square](https://square.github.io/intro-to-d3/)

You can also look at the covid19.ca.gov/equity dashboard chart [source code](https://github.com/cagov/covid19/tree/master/src/js/equity-dash/charts)

### Translations

We integrated a translation pipeline with a human-powered translation service for covid19.ca.gov. Using a javascript charting library that’s part of the page made it easy to integrate all the strings used in the chart labels, legends, and tooltips with the existing site translation services.

This let us deliver a page where each element of the chart is presented in the user’s chosen language. We had never been able to get the translation layer all the way through the data visualization before. The D3-driven charts on covid19.ca.gov/equity/ provide a much better user experience for users of translated versions.

<img src="https://cagov.github.io/covid19.ca.gov-site-handbook/static/img/viet-chart.jpg">

The above screenshot from [California’s commitment to health equity](https://covid19.ca.gov/equity/) shows a chart where all of the internal labels are translated into Vietnamese. 

### Accessibility

D3 charts are elements inside the main page document. We are not embedding them inside separate frames. This makes it easier to enable them to be navigable without a mouse.

We are able to use standard HTML accessibility techniques like tabindex and focus events to allow users to tab into chart elements and interact with the data even if they can’t see the chart itself.

Accessibility tips to consider when using D3:
* Make sure the surrounding page passes accessibility audits. This is a first step, but not sufficient to certify the page because automated audit tools can skip over the data visualization itself.
* Run your own accessibility checks by launching screenreaders locally (command+F5 on Mac).
* Add tabindex to the chart elements you want the user to reach if they’re moving through the page without a mouse.
* Use ARIA labels on purely visual elements like the bars of a bar chart.
* Make any mouse-related events triggered with mouseover also fire on focus so that explanatory tooltips are presented to everybody.

### Responsive sizing

The chart outputs we use on equity are vector graphics. This lets the visuals scale crisply in different sizes. Having an element in the page that’s responsive to existing media queries makes the layout less complicated.

This means we have to take extra care to manage the text sizing inside the charts because it scales with the charts. The text can easily get too small. We’ve set up some chart configurations so that they choose maximum sizes appropriate to specific breakpoints.
