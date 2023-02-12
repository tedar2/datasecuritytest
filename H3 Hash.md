# H3 Hash

## x) Read and summarize: € Schneier 2015: Applied Cryptography: 2.3 One-Way Functions and 2.4 One-Way Hash Functions

The article covers the following topics: 

+ One-way functions
+ Trapdoor one-way function
+ One-way hash functions

### One-way functions

One-way functions play a crucial role in public-key cryptography. They are simple to calculate but hard to reverse, meaning it's easy to compute the output from an input, but hard to find the original input from the output. There is currently no proof that one-way functions exist, but some functions exhibit one-way behavior. However, one-way functions are not suitable for encryption as they cannot be decrypted. Trapdoor one-way functions are a type of one-way function that have a secret trapdoor, making it easy to compute the function in one direction and hard in the other, but the reverse is easy with the secret information. An example is disassembling a watch and putting it back together with instructions.

### One-way hash functions

One-way hash functions, also known as compression functions, contraction functions, message digests, fingerprints, cryptographic checksums, message integrity checks (MICs), and manipulation detection codes (MDCs), play a crucial role in modern cryptography. They work by converting a variable-length input string (known as a pre-image) into a fixed-length output string (known as a hash value). The objective of a hash function is to generate a unique "fingerprint" of the pre-image to determine its similarity with another string.

One-way hash functions are designed to work in one direction only - it is easy to compute the hash value from the pre-image, but it is difficult to generate a pre-image from a particular hash value. The hash function must also be collision-free, meaning it is hard to generate two pre-images with the same hash value. The security of a one-way hash function lies in its one-wayness, as the output is not dependent on the input in any noticeable way.

A message authentication code (MAC) is a one-way hash function with the added benefit of a secret key. The hash value is a function of both the pre-image and the key, meaning only someone with the key can verify the hash value. MACs can be created from hash functions or encryption algorithms, and there are also specialized MACs available.

Sources: [Schneier 2015: Applied Cryptography](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec005)

## a) Install Hashcat

Sources: [Cracking passwords with hashcat](https://terokarvinen.com/2022/cracking-passwords-with-hashcat/)

I have installed the required apps:

+ sudo apt-get update

<img width="729" alt="image" src="https://user-images.githubusercontent.com/90892301/218331690-4d080500-20de-455a-badc-9819db0487f0.png">

+ sudo apt-get -y install hashid hashcat wget

<img width="753" alt="image" src="https://user-images.githubusercontent.com/90892301/218331774-d917e27a-98b5-4edd-a3ba-0f5e2ba84051.png">

+ created new directories

<img width="457" alt="image" src="https://user-images.githubusercontent.com/90892301/218331826-73017933-0e75-4244-8bc5-78279949d4aa.png">

+ installed the big dictionary "Rockyou"

<img width="750" alt="image" src="https://user-images.githubusercontent.com/90892301/218331899-0fd76468-abdd-4702-bb15-56198106ef6e.png">

<img width="627" alt="image" src="https://user-images.githubusercontent.com/90892301/218331950-7c0480ac-bd9d-4efa-a8e0-f581742db4c8.png">

+ Words from the dictionary:

<img width="556" alt="image" src="https://user-images.githubusercontent.com/90892301/218331994-d69069a9-f89c-47ed-8199-fb36d43c3928.png">

<img width="651" alt="image" src="https://user-images.githubusercontent.com/90892301/218332032-642c7f84-e621-4a4a-bdef-6651690c0b5f.png">

+ Identified the hash

<img width="796" alt="image" src="https://user-images.githubusercontent.com/90892301/218332106-9862f6bd-0473-4361-afb0-c58294e57af2.png">

+ Cracked the hash: `hashcat -m 0 '6b1628b016dff46e6fa35684be6acc96' rockyou.txt -o solved>`

<img width="771" alt="image" src="https://user-images.githubusercontent.com/90892301/218332204-3da9a24d-fcd1-4ec6-97ec-d4963ed0d410.png">

## b) Crack this hash: 8eb8e307a6d649bc7fb51443a06a216f

Sources: [Cracking passwords with hashcat](https://terokarvinen.com/2022/cracking-passwords-with-hashcat/)

## c) Compile John the Ripper, Jumbo version

Sources: [Compile John the Ripper, Jumbo version](https://terokarvinen.com/2023/crack-file-password-with-john/)

### d) Crack a zip file password

Sources: [Crack file passwords with John](https://terokarvinen.com/2023/crack-file-password-with-john/)
