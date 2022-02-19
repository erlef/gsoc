## Idea 1: Implementing and evaluating an anti-entropy protocol for riak_core_lite

### Description

Active anti-entropy (AAE) identifies and repairs data inconsistencies between a system's replicas. It is typically implemented as a set of background processes that iterate over the data items, compare their state and trigger synchronisation actions. 
Riak_core_lite currently does not offer an active anti-entropy module.

### Recommended Skills 

* Good programming skills in Erlang
* Basic knowledge about distributed systems

### Mentor(s)

Albert Schimpf, Mariano Guerra, Annette Bieniusa

### Project URL(s)

* https://riak-core-lite.github.io
* Information on AAE in riak: https://docs.riak.com/riak/kv/2.2.3/learn/concepts/active-anti-entropy/index.html