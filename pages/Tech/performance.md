---
title: Performance and accessibility
date: 2021-01-15
permalink: /tech/performance/index.html
toc: true
eleventyNavigation:
  key: Performance and accessibility
  order: 23
  parent: Tech
---

People use a variety of devices in a range of conditions when they try to access web services. This makes it hard to ensure the service works well for everybody. We review all big new features to make sure everyone can use them. We also have automated production monitoring to catch regressions that can sneak in with minor bug fixes.

## New feature development

The Lighthouse audit tools, available as part of Chrome developer tools, help do initial performance and accessibility audits. We shoot for an accessibility score of 100 and a performance score of 100 for desktop and 90 for bandwidth+cpu throttled mobile. The integrated hints feature helps fix the identified problems.

We also:
* Use new features with screen readers ourselves
* Navigate through the flow without using a mouse
* Emulate vision deficiencies (available in chrome dev tools rendering panel)
* Get user testing results from people who use assistive tech regularly when we can

## Production monitoring

We find accessibility problems with Lighthouse, Siteimprove, and Calibre.

Calibre is our most useful performance monitoring tool. It runs automatically every few hours, logs all the performance and accessibility audits for review and reports any changes to slack. We have caught performance regressions in production introduced accidentally with Calibre.

<img src="../../static/img/calibre.jpg" />
