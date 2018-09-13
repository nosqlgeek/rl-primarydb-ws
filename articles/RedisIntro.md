# Redis Introduction

## Single Thread per Instance

A single instance of Redis is basically 

* Single threaded

However, with version 4.0 Redis became more threaded. For now this is limited to deleting objects in the background, and to blocking commands implemented via Redis modules.

A single Redis instance is guaranteeing you 

* To execute the commands in the order 

in which it received them.


You might know other system (i.e. Node.js) those are using an event loop approach.


## 
