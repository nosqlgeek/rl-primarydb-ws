# Redis as a primary Database

This workshop material was created to show some examples for using Redis as your primary database system.

## Agenda

* Intro
   * Workshop Requirements
* Redis OSS Architecture
   * Event Loop
   * Memory First
   * AOF vs. RDB
   * SlaveOf
   * PubSub
   * Modules
   * Sentinel
   * OSS Cluster
* Exercises
   * Establish a Slave-Of link between two Redis instances
   * Configure ‚AOF every write‘ persistence and tail the AOF file
* Redis Enterprise Architecture
   * Basics
   * CRDB & CRDT
   * RoF
* Developing with Redis
   * Introduction
      * Basic Data Structures
      * LUA 
      * Modules
   * Data Structure Deep Dives
      * Strings as Items
      * Hashes as Objects
      * Sets for 1-to-many relationships
      * Hashes as Indexes
      * Sorted Sets as Indexes
      * Sorted Sets for Leader Boards
      * Lists as Queues
      * Hyperloglog for Cardinality Estimations
   * Exercises
      * Implement a simple product catalogue - 45min
   * Modules Deep Dive
      * RediSearch
      * ReJSON
   * Demo
      * Search for a product by name
* Q&A
