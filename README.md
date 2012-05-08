Reonadly
========

A read only distributed database in memory.

In this project, We are going to develop an opensource key-value database running in memory. Nearly all the operations on
this db are read, so we call it a read only db. It's name also came from this read only feature - we mix up 'read' 'only'
to creat a new word: Reonadly.

We develop Reonadly based on some mature db system: Redis, HamsterDB. 

First of all, Reonadly is an embedded database system persisted in memory only. We use HamsterDB or BerkeleyDB's way to
share memory amoung different processes inside one server.

Secondly, Reonadly is a distributed database system accorss different servers. It use Redis or Memcached like protocol to
transfer data between server pairs. 

Thirdly, Reonadly is a key-value db. It does not need to support complex SQL commands or some complex features like 
cursor, secondary index. The most important functionality is find value according a given key. So we use the Redis way to
manage the memory.

Last not the least, we do not have persisitent features or any complex design to gurantee the availibility because the 
master-slave architecture and the read only data set.

Reonadly is quit simple, we try to get rid of most complex things to achieve the highest performance in distributed momory
based key-value database. Of course, in a look-up centric scenarios.