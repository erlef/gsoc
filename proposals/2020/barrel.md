* Website: https://barrel-db.org
* Source code: https://gitlab.com/barrel-db
* Possible mentors: Benoit Chesneau 

Barrel, written in Erlang, brings version control to your data and simplify the development of distributed and modern application such as a conversational platform or blockchain.

Additional ideas by students are welcome!

### # Idea 1: Handle replication using the Yggdrasil Network

* Description: Barrel use [erlang-libp2p](https://github.com/helium/erlang-libp2p) and HTTP to handle the replication in a P2P manner. The idea is to add the support of the Yggdrasil network to handle End-to-end encrypted IPv6 networking.
* Recommended Skills: Erlang
* Mentor: Benoît Chesneau

### # Idea 2: Support Cold/Hot Tiers storage in Barrel

* Description: Barrel uses RocksDB as its storage layer, currently RocksDB support assigns a list of path, newer data is placed into paths specified earlier in the list while older data gradually moves to paths specified later in the list. For example we may use a 300GB fast local SSD as the first path, and a 2TB HDD disk as the second path, and an 16TB remote network disk as the last path. If there is some older but frequently accessed data, it will be cached in memory but need then to handle memory limitations. 
* Recommended Skills: Erlang, RocksDB
* Mentor: Benoît Chesneau

### # Idea 3: Native Erlang Storage

* Description:  Barrel uses RocksDB written in C++ as its storage layer. This could be difficult sometimes to use barrel in embedded world due to platform compatibility issues or limited resources. The idea is to provide a pluggable native storage based for example on Leveled a pure K/V database in erlang to replace it. 
* Recommended Skills: Erlang,
* Mentor: Benoît Chesneau
