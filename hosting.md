---
title: Hosting
layout: recommendation
expires: 2017-11-01
---

GDS follows the [Government Cloud First policy](https://www.gov.uk/guidance/government-cloud-first-policy) meaning that we prefer the use of PaaS and IaaS solutions over managing our own hardware

## User Needs

* Users want systems that are highly scalable and available
* GDS wants to manage the environments easily and simply, with confidence via automated tools

## Principles

GDS will build new tools on a primary cloud platform for each of PaaS and IaaS.

We prefer systems built on a PaaS to systems built on IaaS where possible.

We prefer cloud suppliers that are well supported by common tooling to reduce cost of migrating to a new supplier.

## Tools

GDS has selected two cloud platforms:

### PaaS

* GOV.UK PaaS
  https://cloud.service.gov.uk 

### IaaS

* Amazon Web Services
  https://aws.amazon.com

### Lock in concerns

In order to minimise lock-in, we determine that for the IaaS model, we will use only the core features of AWS that are common with the biggest competitors.  That is to say we will be using  for example: Compute, Networking (load balancing and network segregation), File storage (EBS and S3), Hosted databases (RDS and DynamoDB).

Other platform like services (Cloudfront, Route 53, SQS, SNS, Directory Service and so on) need to be weighed against the lock-in cost before adopting.
