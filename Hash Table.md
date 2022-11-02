## The Hash table data structure stores elements in key-value pairs where

### Key- unique integer that is used for indexing the values
### Value - data that are associated with keys.

## Hashing (Hash Function)
In a hash table, a new index is processed using the keys. And, the element corresponding to that key is stored in the index. This process is called hashing.

## Hash Collision
When the hash function generates the same index for multiple keys, there will be a conflict (what value to be stored in that index). This is called a hash collision



## We can resolve the hash collision using one of the following techniques.

### Collision resolution by chaining
### Open Addressing: Linear/Quadratic Probing and Double Has

## 1. Collision resolution by chaini

In chaining, if a hash function produces the same index for multiple elements, these elements are stored in the same index by using a doubly-linked list.

## 2. Open Addressing

Unlike chaining, open addressing doesn't store multiple elements into the same slot. Here, each slot is either filled with a single key or left NIL.

## Good Hash Functions

A good hash function may not prevent the collisions completely however it can reduce the number of collisions.

## methot to find a good hash function:

### 1. Division Method
### 2. Multiplication Method
### 3. Universal Hashing

## Applications of Hash Table

Hash tables are implemented where:
constant time lookup and insertion is required
cryptographic applications
indexing data is required

## JavaScript Hash Tables

A hash table is an implementation of an associative array, a list of key-value pairs that allow you to retrieve a value via a key. Internally a hash table utilizes a hash function to transform a key value into an index that points to where the value is stored in memory. Hash tables have fast search, insertion and delete operations.

There are two main ways to implement a hash table/associative array in JavaScript.

### 1.Using the Object Data Type
The simplest implementation is using the Object data type.
This is because all non-scalar objects in JavaScript behave as associative arrays,
a mapping from property keys to values. So an Object itself can behave as a basic hash table.


### 2.Using a Map Object
### The Map object was created to implement this type of associative array without some of the downsides of using a basic Object:

There are no pre-existing keys that could result in a collision
A Map object has a size property to track its contents.
A Map object can have keys that are any data type.
A Map has been optimized for repeated addition and insertion of key-value pairs.
A Map object also comes with the following methods:

.clear() Removes all key-value pairs from the Map object.
.delete(key) Deletes the key-value pair and returns true if the key exists. Returns false otherwise.
.get(key) Returns the value associated with key, or undefined if key doesn’t exist.
.has(key) Returns true if key exists, false otherwise.
.set(key,value) Sets the value for the key in the Map object and returns the Map object.










