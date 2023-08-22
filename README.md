# Hash_Table

This repository contains the implementation of Hash Tables in Java using open addressing, 
with the following collision resolution methods: Linear probing, Quadratic probing and Double hashing,
and compare their performance.

## Description
A single element in the Hash Table is an instance from type HashTableElement, containing a key and a value field.

The interface that the hash table needs to implement is IHashTable and includes the following methods:

1. insert(key, value): Inserts an element with the given key and value if there's an available spot in the probing sequence, or throws appropriate exceptions.
2. retrieve(key): Retrieves the HashTableElement with the given key if it exists, otherwise returns null.
3. delete(key): Deletes the element with the given key if it exists, otherwise throws an exception.

### The OAHashTable Abstract Class:
This class implements the IHashTable interface, and has a single abstract method which is  Hash(long key, long i). 
This method implements, for the child classes of OAHashTable, the finding of the i-th member in the search series of key - that is, it returns an index into the search table.

### ModHash Class:
A ModHash Class instance represents a hash function from the family of linear functions of the form ((a*x+b) % p) % m,
where p is prime number and m is the size of the table.

The class should have the following methods:

1. The method 'hash', which evaluates the function on the key value.
2. The static method 'generateRandomFunction', which returns a ModHash object representing a randomly chosen function from the family.

### LPHashTable, QPHashTable, AQPHashTable Classes:
These classes inherit from OAHashTable. These classes used 'hash' functions from the ModHash class.

The classes are as follows:
- LPHashTable for linear probing with a hash table.
- QPHashTable for quadratic probing with a hash table.
- AQPHashTable for alternating quadratic probing.
