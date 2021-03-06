## Idea 1: Erlang LS meets Refactoring

### Description

[Erlang LS](https://github.com/erlang-ls/erlang_ls) is a _language server_ providing language features such as _auto-complete_ or _go-to-definition_ for the Erlang programming language. The server is compatible with Emacs, VSCode, Sublime Text 3, Vim and probably many more text editors and IDEs which adhere to the [LSP protocol](https://microsoft.github.io/language-server-protocol/).

In the Erlang Community, several refactoring tools have been implemented through the years, to help developers refactoring their Erlang code bases. Two notorious refactoring tools are [Wrangler](https://www.cs.kent.ac.uk/projects/wrangler/Wrangler/Home.html) and [RefactorErl](https://plc.inf.elte.hu/erlang/).

Unfortunately, these tools found only limited adoption outside of the academic world, mainly due to the difficulty of integrating them into a regular developer workflow. By integrating refactoring capabilities directly into the editor via Erlang LS, we aim at making refactoring Erlang code bases a smooth experience for developers.

### Recommended Skills

* Erlang knowledge
* Plus: familiarity with concepts such as Abstract Syntax Trees,
  Grammars, etc

### Mentor(s)

Pablo Costas Sánchez - @pablocostass (Klarna)
Roberto Aloi - @robertoaloi (Klarna)

### Project URL(s)

* GitHub repo: https://github.com/erlang-ls
* Docs: https://erlang-ls.github.io
* Proposed list of refactoring transformations to implement: http://pnyf.inf.elte.hu/trac/refactorerl/wiki/RefactoringSteps
