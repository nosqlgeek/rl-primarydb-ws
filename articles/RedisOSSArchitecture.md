# Redis OSS Architecture

## Single Threaded Character

A single instance of Redis is basically 

* Single threaded

However, with version 4.0 Redis became more threaded. For now this is limited to deleting objects in the background, and to blocking commands implemented via Redis modules.

In addition, Redis is forking processes for i.e. snapshotting purposes.

### Event Loop

You might know other system (i.e. Node.js) those are using an event loop approach. Here a simplified code example for an event loop:

```
function main
    initialize()
    while message != quit
        message := get_next_message()
        process_message(message)
    end while
end function
```

### Order of Excution

As a consequence, a single Redis instance is guaranteeing you to execute the commands in the order in which it received them.

## Memory First

Each operation is hitting the

* Memory first

. Redis' eviction is different from RDBM's eviction because 

* All items within a Redis database have to fit into memory 

. An exception is Redis on Flash in Redis Enterprise. 

Further details about the eviction policies can be found here: https://redis.io/topics/lru-cache

## Persistency

There are mainly two persistence options:

* AOF: The append only file persistence logs every write operation received by the Redis server. You can enforce to write to the file for every write operation or every seconds.
* RDB: The RDB persistence performs point-in-time snapshots of your dataset at specified intervals.

Further details can be found here: https://redis.io/topics/persistence

## Replication


You can establish a SlaveOf relationship between 2 Redis instances.

```
SLAVEOF <host> <port>
```
