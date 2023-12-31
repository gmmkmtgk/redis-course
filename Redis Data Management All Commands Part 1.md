# Redis Commands README

## Introduction
This README serves as a concise guide for essential Redis commands, demonstrating their usage in various scenarios.

### 1. Setting and Retrieving Values

#### 1.1 `set name "Keshav Maheshwari"`
Sets the value of the key "name" to "Keshav Maheshwari".

#### 1.2 `get name`
Retrieves the value associated with the key "name".

#### 1.3 `del name`
Deletes the key "name" and returns the number of keys deleted (1 in this case).

#### 1.4 `exists name`
Checks if the key "name" exists, returning 1 if true, and 0 if false.

### 2. Working with Multiple Keys

#### 2.1 `set name1 "Keshav Maheshwari"`
Sets the value of the key "name1" to "Keshav Maheshwari".

#### 2.2 `set name2 "Smiti Maheshwari"`
Sets the value of the key "name2" to "Smiti Maheshwari".

#### 2.3 `get name1` and `get name2`
Retrieve values associated with keys "name1" and "name2" respectively.

#### 2.4 `del name1 name2 name`
Deletes multiple keys ("name1", "name2", and "name") and returns the total number of keys deleted.

### 3. Setting Time-to-Live (TTL) for Keys

#### 3.1 `set name "Smiti Maheshwari" ex 120`
Sets the value of the key "name" with an expiration time of 120 seconds.

#### 3.2 `ttl name`
Returns the remaining Time-to-Live in seconds for the key "name".

#### 3.3 `expire name 10`
Sets the expiration time for the key "name" to 10 seconds.

#### 3.4 `pexpire name 100000`
Sets the expiration time for the key "name" in milliseconds.

#### 3.5 `persist name`
Removes the expiration time from the key "name," making it persistent.

### 4. Miscellaneous Commands

#### 4.1 `keys *`
Lists all keys in the current database.

#### 4.2 `select <db>`
Switches to the specified database.

## Conclusion
This README provides a quick reference for common Redis commands and their usage in different scenarios. Use it as a guide for working with Redis in your applications.
