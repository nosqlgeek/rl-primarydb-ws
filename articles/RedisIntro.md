# Redis Introduction

## Single Threaded Character

A single instance of Redis is basically 

* Single threaded

However, with version 4.0 Redis became more threaded. For now this is limited to deleting objects in the background, and to blocking commands implemented via Redis modules.

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
