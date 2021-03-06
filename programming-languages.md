---
title: Programming languages
layout: recommendation
expires: 2017-10-01
---

We want to use a range of programming languages at GDS because we think
using the right tool for the job will give us the best chance of building
services that best meet users’ needs. This document does not apply to
choosing 'off the shelf' software (open source or not).

We want to focus on using a small number of programming languages for
core software development tasks.

This should make it easier for developers to:

- move around the organisation
- develop shared components
- improve their personal development
- master how they operate applications

## Using Java, Python and Ruby as our core languages

Our core languages are __Java, Python and Ruby__.

We've chosen these 3 languages because they are successfully used by
teams at the moment, and we are confident in how to host and operate
applications written in them. We'd advise you to carry out new
development in one of them.

## Code styleguides

Developers read code much more often than they write it. These guidelines
are intended to improve the readability of code and make it consistent
across GDS projects.

A style guide is about consistency. Consistency with this style guide is
important. Consistency within a project is more important. Consistency within
one module or function is most important.

But most importantly: know when to be inconsistent -- sometimes the style guide
just doesn't apply. When in doubt, use your best judgement. Look at other
examples and decide what looks best. And don't hesitate to ask!

Some good reasons to ignore a particular guideline:

- When applying the guideline would make the code less readable, even for
  someone who is used to reading code that follows this style guide.
- To be consistent with surrounding code that also breaks it (maybe for
  historic reasons) -- although this is also an opportunity to clean up the
  existing code.
- Because the code in question predates the introduction of the guideline and
  there is no other reason to be modifying that code.
- When the code needs to remain compatible with older versions that
  don't support the feature recommended by the style guide.

We've got a consistent style for [Ruby](programming-languages/ruby.html) and will
add a guide for Python and Java.

## Languages in use in specific contexts

### JavaScript

We write server-side JavaScript with [Node.js][nodejs].
The service manual has information on
[using client-side JavaScript][manual_js].

[nodejs]: https://nodejs.org/
[manual_js]: https://www.gov.uk/service-manual/technology/using-progressive-enhancement

GDS projects that use Node.js include:
GOV.UK Frontend, GOV.UK Pay and the Performance Platform.

These projects have made the decision to use Node.js, and the tech forum is watching the output of this. No new projects should use Node.js without prior consultation with the Deputy Director Technology Operations.

Node.js can be used to render a web interface for your service but should
not be used to implement any significant ‘application logic’. For instance
GOV.UK Pay has created thin, client-facing applications that do not store
data (although they may retrieve data from an API).

In the past we've had problems operating and maintaining products written in
Node.js (for example maintaining dependencies, picking the appropriate
libraries to use, understanding the appropriate application structure, and
ensuring security of the code). We suspect that this is because:

- It's younger and less mature than Java, Python and Ruby
- We have fewer developers with Node.js skills than other tools we use

Node.js is now frequently used in the wider software development ecosystem for
building web application frontends. This increase in Node.js use means there
has been a growth in  skills and supporting tools and we expect this to continue.
This means we may reevaluate it as a core language in the future.

Teams that adopt Node.js must take steps to ensure that they have access to
sufficient developers with Node.js experience.

### Go

The GOV.UK router is built using Go, and it's the core language for Cloud
Foundry which runs our Platform as a Service.

Go is an appropriate language for some systems programming, like proxying,
routing and transforming HTTP requests. However, since we don't maintain much
Go and thus are likely to have few people with the skills to do so, any such
code poses a significant risk. Components should only be written in Go if
there is no alternative maintained open source tool which could be used, and
after a team has developed a plan to ensure that it will have the skills to
maintain the component in future.

## Languages we won't use for new projects

We used __Scala__ in the early days of GDS. GOV.UK Licensing is the only remaining
application written in Scala but we've found it hard to support because of a lack
of skills in GDS and we’re planning to rewrite it. Do not use Scala for new projects.

## Using other languages

There will be sensible reasons to not follow the above guidance on languages.
For example when you're:

- extending an existing codebase or ecosystem
- scripting in a particular environment
- experimenting during an alpha (with an expectation that it's replaced by something we have more confidence in for beta)
- working in a very specific or unusual problem domain, like heavy use of WebSockets

The set of languages we're comfortable supporting will change over time.

If you want to use a new language, talk to your technical architect and the
Deputy Director Technology Operations and then create
a prototype. If it goes well make a pull request to change this document.

If you've had problems using one of the languages we support, make a pull request to
document the issues you've had.
