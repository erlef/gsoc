## Idea 1: Zotonic - Elixir integration

### Description

Zotonic is the Erlang Content Management System and Framework.

It provides a complete environment to build web sites, with integrated administrative
environment, module system, virtual hosting, users, media, content management,
templates, emailing, LetsEncrypt, etc.

We would like to make modules and sites with Elixir.

For this:

* The build system (rebar3) must know how to handle Elixir applications;
* The runtime module and site managers must be able to introspect Elixir modules;
* The template compiler must be able to call into Elixir modules for filters and such;
* The MQTT routines must understand models implemented in Elixir;
* The notification system must understand observers written in Elixir;
* The `zotonic_filehandler` must understand how to compile Elixir files and/or projects.

And probably some other changes here and there to make it a smooth experience for Elixir developers.

### Recommended Skills

Experience with Elixir and Erlang. You must be willing to investigate how Elixir functions
are called from Erlang and dive into the runtime behavior of the Beam.

### Mentor(s)

Marc Worrell @mworrell
Maas-Maarten Zeeman @mmzeeman
With help from Arjan Scherpenisse @arjan

### Project URL(s)

https://github.com/zotonic/zotonic