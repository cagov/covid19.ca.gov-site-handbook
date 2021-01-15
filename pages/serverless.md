---
title: Serverless APIs
date: 2021-01-15
permalink: /tech/serverless/
toc: true
eleventyNavigation:
  key: Serverless APIs
  order: 48 
  parent: Tech
---

The covid19.ca.gov site runs dozens of builds a day to release normal data and content updates. Widgets that depend on more dynamic datasets make calls to backend APIs to retrieve query results.

We use Functions As A Service (FAAS) to run backend code in a serverless pattern. The covid19.ca.gov infrastructure is run on Azure functions. This is similar to AWS Lambda. FAAS provides a runtime for code which is ephemeral.

These tools are the fastest way to scale up and down in response to varying load. New FAAS instances are created quickly in response to requests and destroyed when idle for a few minutes. All up and down scaling management is part of the cloud platform. This frees developers from managing the orchestration of any upkeep of the runtime environment.

Benefits
* Built-in scaling
* Built-in runtime management
* Fastest way to let backend code ramp up and down based on request volume
* Low cloud cost
* Faster development workflows

## Use cases

Serverless patterns are not appropriate for long-running or computationally intensive tasks. These programs run more efficiently on longer-lived platforms with more flexible CPU/memory configurations. Serverless shines in bursty, high volume short workloads like receiving a request for data, querying a data source, and transforming and returning json. 

## Outsourcing of complexity

The development workflow speed wins are due to developer convenience. A developer is able to build an API by writing a function that contains mostly business logic and deploy this in seconds to a solid platform. This allows them to focus on team goals instead of managing infrastructure complexity.
