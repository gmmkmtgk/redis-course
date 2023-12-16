# Redis Command Reference

This README file provides a reference guide for using Redis commands with examples.

## Table of Contents
- [Connecting to Redis](#connecting-to-redis)
- [Key-Value Operations](#key-value-operations)
- [Key Manipulation](#key-manipulation)
- [Expiration and TTL](#expiration-and-ttl)
- [Key Search and Pattern Matching](#key-search-and-pattern-matching)
- [Database Selection](#database-selection)
- [Server Information](#server-information)
- [Persistence](#persistence)
- [System Commands](#system-commands)
- [Data Types](#data-types)
- [Set Operations](#set-operations)

## Connecting to Redis
To connect to the Redis server, use the `redis-cli` command.

```bash
$ redis-cli
```

## Key-Value Operations
### SET
Set a key to hold a string value.

```redis
127.0.0.1:6379> set name "Keshav Maheshwari"
OK
```

### GET
Get the value of a key.

```redis
127.0.0.1:6379> get name
"Keshav Maheshwari"
```

### DEL
Delete one or more keys.

```redis
127.0.0.1:6379> del name
(integer) 1
```

## Key Manipulation
### RENAME
Rename a key.

```redis
127.0.0.1:6379> rename name surname
OK
```

### TYPE
Determine the data type of a key.

```redis
127.0.0.1:6379> type name
string
```

## Expiration and TTL
### EXPIRE
Set a key's time to live in seconds.

```redis
127.0.0.1:6379> expire name 10
(integer) 1
```

### TTL
Get the time to live for a key in seconds.

```redis
127.0.0.1:6379> ttl name
(integer) 8
```

## Key Search and Pattern Matching
### KEYS
Find all keys matching a pattern.

```redis
127.0.0.1:6379> keys *
1) "hello"
2) "keshav2"
3) "keshav"
4) "dota2"
```

### SCAN
Incrementally iterate the keyspace.

```redis
127.0.0.1:6379> scan 0
1) "0"
2) 1) "hello"
   2) "keshav2"
   3) "keshav"
   4) "dota2"
```

## Database Selection
### SELECT
Change the selected database.

```redis
127.0.0.1:6379> select 1
OK
127.0.0.1:6379[1]> get key1
(nil)
```

## Server Information
### INFO
Get information and statistics about the server.

```redis
127.0.0.1:6379> info
# Server
redis_version:7.2.3
...
```

## Persistence
### SAVE
Synchronously save the dataset to disk.

```redis
127.0.0.1:6379> save
```

### BGSAVE
Asynchronously save the dataset to disk.

```redis
127.0.0.1:6379> bgsave
```

## System Commands
### SHUTDOWN
Shutdown the Redis server.

```redis
127.0.0.1:6379> shutdown nosave
```

## Data Types
### LIST
```redis
127.0.0.1:6379> lpush surnames mah
(integer) 1
```

### SET
```redis
127.0.0.1:6379> sadd k1 v1
(integer) 1
```

## Set Operations
### UNLINK
Unlink one or more keys.

```redis
127.0.0.1:6379> unlink key1 key2
(integer) 2
```

### FLUSHALL
Remove all keys from all databases.

```redis
127.0.0.1:6379> FLUSHALL
OK
```

This README provides a basic overview of Redis commands. Refer to the official [Redis Command Reference](https://redis.io/commands) for more detailed information.
