## Idea 1: Hex web auth flow

### Description

Hex is a package manager for the Erlang VM.

Currently there are two terminal applications capable of publishing and managing packages, mix and rebar3_hex. Sadly, they vary a bit in some aspects while registering an user and in both the auth flow could be improved by moving from a password prompt towards a web auth flow, where the user would put their credentials and the auth token would be generated on the website and pushed back to the terminal.

For this to be achieved, the following should be done:

* Both `mix` and `rebar3_hex` should have an unified user registration experience
* Align with `hexpm` on flow and low level specifications
* Support in `hex_core` the new API that will be described and detailed in the above task
* Work the new `hex_core` API offerings into to `mix hex`
* Work the new `hex_core` API offerings into `rebar3_hex`

### Recommended Skills

Erlang and Elixir. The biggest chunk of work will require Elixir skills, Erlang is needed for `hex_core` and `rebar3_hex`

### Mentor(s)

* Bryan Paxton
* Todd Resudek*

> \* Todd's availablily is tentative, it depends on the timezone of the student involved.

### Project URL(s)

https://github.com/erlef/build-and-packaging-wg/issues/21