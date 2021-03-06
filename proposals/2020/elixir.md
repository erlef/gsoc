* Website: https://elixir-lang.org
* Source code: https://github.com/elixir-lang/elixir
* Ideas are listed in no particular order

### Idea #1: Two-Factor Authentication for Hex

Implement Two-Factor Authentication for package publishing in Hex.pm.

**Expected results:** 2FA implementation for Hex.pm (server), Hex (client), possibly rebar3 (via hex_core)

**Knowledge prerequisites:** Elixir. If time permits, contributions to rebar3 (via hex_core) are also welcome. Both are written in Erlang.

**Possible Mentors:** Eric Meadows-Jönsson, Todd Resudek

### Idea #2: Package vulnerability disclosure for Hex

Add the ability to report vulnerabilities in Hex packages via a form on the https://hex.pm/ website. A group of trusted moderators will be notified that will either accept or reject the report, if accepted the package owners will be notified. After the fix is released, or after a deadline passes, a security advisory will be posted for the package. A good proposal would describe what other features could be part of the project.

**Expected results:** A website form to report vulnerabilities and an interface for the moderators to triage reports and post security advisories.

**Knowledge prerequisites:** Elixir and Phoenix web framework

**Possible Mentors:** Eric Meadows-Jönsson, Wojtek Mach

### Idea #3: Extend Makeup (the syntax highlighter used by ExDoc) with support for new languages

ExDoc supports syntax highlighting thanks to the Makeup package. The way to add support for new language is to write new lexers (one lexer per language). Currently the only languages supported are Elixir and Erlang.

The goal of this idea is to implement lexers with support for new languages. Some suggested languages are HTML, JavaScript, CSS, and SQL.

Other languages may be added. Implementing lexers is relatively time-intensive, and someone working full time for 12 weeks can probably make impressive progress. The complexity of the task will depend on the lexer. Of the proposed languages, HTML is most likely the easiest (so a great starting point), JavaScript the hardest.

**Expected results:** Implement new Makeup lexers for different languages.

**Knowledge prerequisites:** Elixir. Familiarity with [the NimbleParsec library](https://github.com/dashbitco/nimble_parsec/) is helpful, but developers can also get comfortable with it when coding starts. Very basic knowledge of the languages the lexers will be implemented for is also welcome. 

Mentors: Tiago Barroso, José Valim
