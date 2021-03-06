* Website: https://rebar3.org
* Source code: https://github.com/erlang/rebar3

Rebar3 is the standard build tool within the Erlang community. It essentially bundles all of the other tools shipping with Erlang along with a few open-source ones, and makes them all work under a unified project structure.
It also supports pluggable compiler back-ends and acts as the build tool of many other languages on the BEAM virtual machine.

### Idea 1: Monorepo usage patterns

#### Description

Rebar3 focuses a lot of its usage on open-source usage with [external dependencies](https://adoptingerlang.org/docs/development/dependencies/#rebar3-expectations) and a limited set of [releases](https://adoptingerlang.org/docs/development/otp_high_level/). This works well for open-source developers and for corporations that use multiple repositories for their development, but has proven painful when organizations rely on a [monorepo](https://en.wikipedia.org/wiki/Monorepo) pattern.

In monorepos, Rebar3 ends up scanning and re-building too many applications and releases, and generally takes a long time without being particularly pleasant to use. This is due to a few common problems:

* Organizations with Monorepos have a lot of private code in there and are not willing to share that content with Rebar3 maintainers; in turn, performance and usability testing is more complex
* Organizations with monorepos tend to have some custom tooling that isn't necessarily standardized and is difficult to plan for. Finding the appropriate minimal amount of support to ease monorepo pain is a bit of an open problem
* Many groups have managed to make monorepos work by "abusing" features in ways they were never intended (i.e. [_checkout dependencies](https://www.rebar3.org/docs/dependencies#section-checkout-dependencies) to make individual project see all of the parent libraries all the time) and we want to give them the proper tool for the job
* Monorepos tend to often rely on specifying subsets of libraries on which to operate. Rebar3 is built assuming the directory it's called in represents a whole project; this assumption is furthermore encoded into almost all tasks (compiling, releasing, testing, code analysis, etc.), including plugins provided by the community. We can therefore not just add back a list of applications on which to operate to all Rebar3 tasks.

For this project, we have identified the need for:

* A sample monorepo project, which contains hundreds or thousands of generated libraries of all kinds, with various inter-dependencies and ideally a broad usage of most Rebar3 features. This project would represent a test bed for usability, benchmarking (memory and time), and functionality of any future monorepo development
* Proposals for prototype approaches to solving the monorepo problem without majorly impacting the existing workflow of other users (we have a few ideas to provide and discuss already)
* Prototyping and evaluating potential solutions
* Driving a promising solution to production so that large organizations can rely on them  

#### Recommended Skills
Erlang

#### Possible Mentors

* Fred Hebert
* Pablo Costas Sánchez

### Idea 2: Rebar3 Dependency Reduction

#### Description

In an attempt to bring ourselves closer to  being an official build tool included with the Erlang programming language, one of the starting steps is to find out how we can reduce the number of dependencies required for the tool. This task will require doing careful surgery on rebar3, a tool with a strong commitment to backwards compatibility with thousands of users.

#### Recommended Skills
Erlang

#### Possible Mentors

* Fred Hebert
* Pablo Costas Sánchez