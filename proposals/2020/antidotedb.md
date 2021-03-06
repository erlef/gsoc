* Website: https://www.antidotedb.eu/
* Source code: https://github.com/antidotedb
* Possible Mentors: Annette Bieniusa

AntidoteDB is a highly-available and scalable geo-replicated datastore. Its data model are conflict-free replicated datatypes (CRDTs) that can be accessed in a transactional causally consistent way. Antidote is an open-source project that has evolved from the European research projects Syncfree and Lightkone.

Additional ideas by students are welcome!

### Idea #1: Support for Elixir

Antidote offers a number of different bindings for languages, the Erlang binding is the one covering most functionality today. We want to investigate how we can make Antidote easily accessible to Elixir programmers.

**Knowledge prerequisites:** Basic knowledge of Erlang/Elixir

### Idea #2: Improving coverage for dialyzer and unit tests

Type annotations provide an important guidance to programmers that are new to Erlang code. In this project, you will clean-up and improve the types in Antidote and get our unit test coverage up.

**Knowledge prerequisites:** Knowledge of Erlang/OTP

### Idea #3: Property-based testing for Antidote

We are currently decomposing into different components for persistent storage, inter-DC communication, transaction management, frontend, etc. which are stateful and therefore difficult to cover with simple unit tests. In addition to the unit and systems tests that are already in place, we want to add property-based tests.

**Knowledge prerequisites:** Knowledge of Erlang/OTP

### Idea #4: Security

In this project, you will add an authentication mechanism to Antidote. Further tasks will be to make the inter-DC communication secure.

**Knowledge prerequisites:** Knowledge of Erlang/OTP, background knowledge on security