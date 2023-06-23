# Hash Table

## what is it and how it's work

also known as a hash map, is a data structure that allows efficient insertion, deletion, and retrieval of key-value pairs. It uses a technique called hashing to map keys to array indices, providing constant-time average case complexity for these operations.

The Hash table data structure stores elements in key-value pairs where

Key- unique integer that is used for indexing the values
Value - data that are associated with keys.


### Hashing (Hash Function)
In a hash table, a new index is processed using the keys. And, the element corresponding to that key is stored in the index. This process is called hashing.

Let k be a key and h(x) be a hash function.

Here, h(k) will give us a new index to store the element linked with k.

```
For any set of objects S and any integer
m > 0, a function h : S → {0, 1, . . . , m − 1}
is called a hash function.
m is called the cardinality of hash function h.

```
Desirable Properties
- Hash function should be fast to
compute
- Different values for different objects
- Direct addressing with O(m) memory
- Want small cardinality m
- Impossible to have all different values if
- number of objects |S| is more than m
(by pigeonhole principle)

###  what is hashing 
it's algorithm that take a string and convert it to something is an clear from letters and numbers for security reasonse

### A bucket
 is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.


[has](./Hash-2_0.webp)
### Collisions
When the hash function generates the same index for multiple keys, there will be a conflict (what value to be stored in that index). This is called a hash collision.

We can resolve the hash collision using one of the following techniques.

Collision resolution by chaining
Open Addressing: Linear/Quadratic Probing and Double Hashing

`When h(o1) = h(o2) and o1 ̸= o2, this is a`

## Methods
set()
When adding a new key/value pair to a hashtable:

send the key to the hash() method.
Once you determine the index of where it should be placed, go to that index
Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
If something does exist, add the new key/value pair to the data structure within that bucket.
get()
The get() method takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

has()
The has() method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the hash() method and check the hashtable if the key exists in the table given the index returned.

keys()
The keys() method returns a collection (array) of unique hash keys.

hash()
The hash() method will accept a key as a string, conduct the hash, and then return the index of the array 
where the key/value should be placed.


The efficiency of a hash table depends on the distribution of the hash codes and the quality of the hash function. A good hash function should evenly distribute the keys across the array to minimize collisions and ensure efficient operations.

Overall, a hash table provides fast access to data by leveraging the hash codes and indexing techniques. It is widely used in various applications, including caching, indexing, and data storage.

## In Python, you can create a hash table using a dictionary data structure, which is implemented as a hash table itself


## Applications of Hash Table

Hash tables are implemented where

constant time lookup and insertion is required
cryptographic applications
indexing data is required