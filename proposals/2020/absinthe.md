* Source code: https://github.com/absinthe-graphql/absinthe

### Idea #1: Implement a tracing library for Absinthe GraphQL

[GraphQL](https://graphql.org/) is a modern query language for writing APIs. In the Elixir world GraphQL schema definitions and the runtime are implemented using the [Absinthe](https://hexdocs.pm/absinthe) library. Absinthe is an extensible toolkit that provides a flexible way (through middlewares and pipelines) of controlling how queries are resolved.

A standard implementation of GraphQL tracing is provided by [Apollo Engine](https://www.apollographql.com/docs/graph-manager/performance/#traces), which has some support in Absinthe, but a deprecated [proxy](https://www.apollographql.com/docs/references/engine-proxy/) is needed to send data to the backend since there currently is no production-ready implementation of this in Elixir. Apart from a [library](https://github.com/maartenvanvliet/absinthe_trace_reporter) that provides partial support.

It would be useful to have an integration with an open source tool, for example, Jaeger or Zikpin. Preferably an implementation that supports OpenTracing (merged with OpenCensus as OpenTelemetry). A good starting point may be [Tapper](https://github.com/Financial-Times/tapper), especially [Tapper Absinthe Plug](https://hexdocs.pm/tapper_absinthe_plug/readme.html) which did not change in a while, so it may not support the latest Absinthe. The goal is to implement a library that is easy to use and requires minimal changes to the Absinthe schemas for integration. This can likely be achieved through the use of Absinthe middlewares, custom phases and pipelines.

Additionally, the trace context may be exposed in the GraphQL resolution struct, so resolvers can create spans and pass the context to other functions/services.

**Expected results**: A library that integrates with Absinthe and sends tracing information to a server (preferably one that supports OpenTracing). Using the library should require minimal change to existing code. The destination of trace data and the required credentials should be configurable.

**Knowledge prerequisites**: Elixir required; OpenCensus and/or OpenTracing and GraphQL knowledge is useful, but can be obtained during the project

**Possible mentors**: Laszlo Hegedus