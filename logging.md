---
title: Logging
layout: recommendation
expires: 2017-09-01
---

## Shared logging platform

The service support and operations team is investigating whether
we should run a shared logging platform for product teams at GDS.

If you're about to start some work on logging, ask in the
[#tech-ops-forum Slack channel](https://govuk.slack.com/messages/tech-ops-forum/)
whether there's something you can use.

## Sumo Logic

Some teams have used [Sumo Logic](https://www.sumologic.com/)
successfully for storing and querying logs.

## Elasticsearch, Logstash and Kibana (ELK)

Each team should not operate its own ELK stack for logging.
In the past we've found that ELK is relatively easy to set up
but teams tend to not prioritise keeping it updated.

ELK isn't appropriate for long term archival of logs. There
are services which are less expensive and more reliable.
