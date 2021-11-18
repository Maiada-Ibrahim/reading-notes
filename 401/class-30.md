# Hash Tables
Hashtables are a data structure that utilize key value pairs. This means every Node or Bucket has both a key, and a value.
- A hash table is an unordered collection of key-value pairs, where each key is unique.
- Buckets - A bucket is what is contained in each index of the array of the hashtable. 

- Collisions - if key get hasshed to the same location what to do so Collisions are solved by changing the initial state of the buckets. Instead of starting them all as null that mean two calls to .Add(key, val) with different keys would overwrite each other. 

- hash is the ability to encode the key that will eventually map to a specific location in the data structure that we can look at directly to retrieve the value.

- The same key should always produce the same hash code.

![](https://miro.medium.com/max/1200/1*J7lzku84LsxaeXpbgqRy5Q.png)

Creating a Hash
- created your array of the appropriate size,
- Add or multiply all the ASCII values together.
- Multiply it by a prime number such as 599.
- Use modulo to get the remainder of the result, when divided - by the total size of the array.
- Insert into the array at that index.


Inserting a new record (key, value) is a two-step procedure:

- we extract the three last digits of the key, hash = key % 1000,

- and then insert the key and its value into the list located at table[hash].

Insert
Implementation of hash table with linear probing

     void insert(string s)
    {
        //Compute the index using the hash function
        int index = hashFunc(s);
        //Search for an unused slot and if the index will exceed the hashTableSize then roll back
        while(hashTable[index] != "")
            index = (index + 1) % hashTableSize;
        hashTable[index] = s;
    }

to read value:

- accept a key
- calculate the hash of the key
- use modulus to convert the hash into an array index
- use the array index to access the short LinkedList  representing a bucket
- search through the bucket looking for a node with a key/value pair that matches 1. the key you were given



# Bucket Sizes

- the load factor it tell us the size (how full the hash table is)


 - A hash table can start with only a few buckets, calculate it’s own load factor, recognize when it gets too full and automatically grow and add more buckets to itself to accommodate more data

### Internal Methods
- Add() When adding a new key/value pair to a hashtable:

send the key to the GetHash method. then determine the index then go to that index Check if something exists at that index already, if it doesn’t, add it with the key/value pair. that bucket.

- Find() The Find takes in a key, gets the Hash, and goes to the index location specified.

- Contains() The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. 

- GetHash() The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

