# H3 Hash

## x) Read and summarize: € Schneier 2015: Applied Cryptography: 2.3 One-Way Functions and 2.4 One-Way Hash Functions

The article covers the following topics: 

+ One-way functions
+ Trapdoor one-way function
+ One-way hash functions

### One-way functions

One-way functions play a crucial role in public-key cryptography. They are simple to calculate but hard to reverse, meaning it's easy to compute the output from an input, but hard to find the original input from the output. There is currently no proof that one-way functions exist, but some functions exhibit one-way behavior. However, one-way functions are not suitable for encryption as they cannot be decrypted. Trapdoor one-way functions are a type of one-way function that have a secret trapdoor, making it easy to compute the function in one direction and hard in the other, but the reverse is easy with the secret information. An example is disassembling a watch and putting it back together with instructions.

### One-way hash functions