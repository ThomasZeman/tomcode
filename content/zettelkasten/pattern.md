---
title: "Horizontal and Vertical Scaling"
date: 2020-01-01
draft: false
author: Tom
lightgallery: true
---
## Definition

[Christoph Alexander](https://en.wikipedia.org/wiki/Christopher_Alexander) introduced patterns as part of his work as a real-world architect. His [definition](https://en.wikipedia.org/wiki/Design_pattern) of a pattern language and a pattern is:

``The elements of this language are entities called patterns. Each pattern describes a problem that occurs over and over again in our environment, and then describes the core of the solution to that problem, in such a way that you can use this solution a million times over, without ever doing it the same way twice.``

Another popular and shorter definition is: "A pattern is a reusable solution to a recurring problem in a given context."

 A pattern description contains the following properties:

- Pattern name
- The context in which the pattern is applicable
- An example
- A short description of the problem it is solving
- Forces on the solution that need to be considered
- The solution to the problem
- Consequences of the solution; benefits; liabilities
- Optional: Related patterns
- Optional: Anti-patterns

## Example ''Cache''


|Property|Description|
|--|--|
|Name|Cache|
|Context|Upon request, a service performs a CPU intensive task and returns a result|
|Example|A weather forecast service takes a geographical location, calculates and returns the rain forecast for tomorrow based on current radar data
|Problem|The calculation is expensive and should not be executed twice for the same location
|Forces|The result of the calculation changes over time as new radar images become available
|Solution|Save the outcome of the calculation for a particular place in a database. When there is already a result stored in the database for any new request, return this instead. Remove entries in the database after a given time to avoid returning stale results.
|Consequences|Benefits: Queries for the same location become much faster. Double calculations are avoided. Liabilities: Clients could get stale results when the first calculation happened too long ago. Results in the database need to be removed after a while.

