This page includes miscellaneous ideas about new exciting projects that can be built on top of the Erlang Ecosystem. 

Ideas are listed in no particular order.

### Idea #1: PlantUML support

[PlantUML](https://plantuml.com/) is a GPL-licensed tool that relies on Graphviz to generate graphic representations (namely, UML diagrams) from text files. I'd dare say its popularity is on the increase, as I've seen it adopted as one of the options for C4 (the architectural notation https://c4model.com/), which built their own "DSL" of sorts on top of PlantUML. The text description is easy to write and read, frees the user/developer from the burden of "graphically placing the elements on the diagram" (which is taken care of by Graphviz*), and hence encourages a workflow where this sort of artifacts are kept up-to-date with reduced effort.

A tool like the one suggested, that could automatically produce, either from Erlang/Elixir code, the PlantUML text file that would represent either a [gen_statem](https://erlang.org/doc/man/gen_statem.html) or Property Based Testing state machine would be the goal of this idea. Or conversely, that from a PlantUML text file a skeleton of Elixir/Erlang code for a process with the represented states and accepted messages.

**Requirements:** Elixir/Erlang knowledge. UML knowledge is not a hard requirement, but it would help in understanding PlantUML. And depending on the applicant familiarity with the plugin systems of IDEs like Eclipse or VS, the tool could materialize as one of those. 

**Knowledge prerequisites:** Laura Castro, Bryan Hunt