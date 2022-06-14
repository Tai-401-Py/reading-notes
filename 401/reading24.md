# [Hashtables](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-30/resources/Hashtables.html)

## What is a hashtable

    A hashtable is a datastructure that utilizes key/value pairs. This means every Node or Bucket has both key and value. 

### Hashing

    A hashtable is created from an array. It's important  to have a good sized one to account for index placements. After you create that table, you create a key to dictate placement in the table. here are some ways to calculate it. 

1. Add or multiply all the ASCII values together.
2. Multiply it by a prime number such as 599.
3. Use modulo to get the remainder of the result, when divided by the total size of the array.
4. Insert into the array at that index.


### Collisions

A collision occours when more than one key hashes to the same index, the worst possible hash is one that indexes everything to the same index.

Hash maps do this to store values:

- accept a key
- calculate the hash of the key
- use modulus to convert the hash into an array index
- store the key with the value by appending both to the end of a linked list

Hash maps do this to read value:

- accept a key
- calculate the hash of the key
- use modulus to convert the hash into an array index
- use the array index to access the short LinkedList representing a bucket
- search through the bucket looking for a node with a key/value pair that matches the key you were given

### Internal Methods

`Add()` When adding a new key/value pair to a hashtable:

- send the key to the GetHash method.
- Once you determine the index of where it should be placed, go to that index
- Check if something exists at that index already, if it doesn’t, add it with the key/value pair.
- If something does exist, add the new key/value pair to the data structure within that bucket.

`Find()`

- The Find takes in a key, gets the Hash, and goes to the index location specified. Once at the index location is found in the array, it is then the responsibility of the algorithm the iterate through the bucket and see if the key exists and return the value.

`Contains()`

- The Contains method will accept a key, and return a bool on if that key exists inside the hashtable. The best way to do this is to have the contains call the GetHash and check the hashtable if the key exists in the table given the index returned.

`GetHash()`

- The GetHash will accept a key as a string, conduct the hash, and then return the index of the array where the key/value should be placed.

### Handling Collisions

you can make use of a linked list in order to handle collisions and this is called chaining. 