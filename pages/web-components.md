---
title: Widgets as web components
date: 2021-01-15
permalink: /tech/web-components/
toc: true
eleventyNavigation:
  key: Widgets as web components
  order: 22
  parent: Tech
---

Web components are the W3C standardized browser component model. Encapsulating front end functionality into components used to require an underlying framework. 

We take advantage of the fact that 98% of browsers support web component features without requiring any polyfills. This gives us the benefits of componentization without using heavy underlying libraries.

The main benefits of using web components are:
* Performance
* Code encapsulation
* Code portability
* Able to be tested in isolation

The most important benefit of web components  is the ability to define custom elements. 

One example is a new HTML tag like:

```<cagov-accordion />```

These tags are associated with new functionalities we write in new classes.

These extend the HTMLElement class so our tags can take advantage of all the standard browser element features. For example, the new tag is an element in the DOM. This lets us assign complex objects as properties and access these objects with this.objectReference. Custom elements come with their own set of [instantiation and change events](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Using_custom_elements#using_the_lifecycle_callbacks).

There are several secondary benefits too. For example, it’s easy to delete them because each component is isolated in its own class with a known API. This makes it safe to remove them when they’re no longer needed.

We’ve documented the [components we’ve created](https://wonderful-plant-07a82e81e.azurestaticapps.net/?path=/story/welcome--pagegb) in our interactive component library
