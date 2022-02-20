* Website: https://rebar3.org
* Source code: https://github.com/erlang/rebar3

Rebar3 is the standard build tool within the Erlang community. It essentially bundles all of the other tools shipping with Erlang along with a few open-source ones, and makes them all work under a unified project structure.
It also supports pluggable compiler back-ends and acts as the build tool of many other languages on the BEAM virtual machine.

### Idea 1: Rebar3 Dependency Reduction

#### Description

In an attempt to bring ourselves closer to  being an official build tool included with the Erlang programming language, one of the starting steps is to find out how we can reduce the number of dependencies required for the tool. This task will require doing careful surgery on rebar3, a tool with a strong commitment to backwards compatibility with thousands of users.

#### Recommended Skills
Erlang

#### Possible Mentors

* Fred Hebert
* Bryan Paxton
* Pablo Costas Sánchez