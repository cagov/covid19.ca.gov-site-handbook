---
title: Static site pregeneration
date: 2021-01-15
permalink: /tech/ssg/
toc: true
eleventyNavigation:
  key: Static site pregeneration
  order: 24
  parent: Tech
---

We combine authoring in WordPress with deployment using 11ty as a static site generating build step. This gives us a mature, refined content management tool and a bulletproof, low hassle production architecture.

The biggest benefit of static site pregeneration is it reduces the infrastructure required to host web content in production. Static site pregeneration allows a production server to be replaced by a S3 like file host backed CDN.

Other benefits include:
* Less single points of failure in production
* Reduced attack surface
* Cheaper cloud hosting cost
* Built in cross region scalability
* Higher SLA from cloud provider
* Portability (the site can switch CMS tools or cloud providers)

We set up workflows that listen for changes in our WordPress site and pull updates into our github repository. Each change to our repository triggers our git action workflow, which runs build tests before merges. Merged changes trigger a production build and deploy task run in a git action that regenerates the entire site and deploys to the target environment.
