# h4 Uryyb Greb

## x) Read and summarize - Schneier 2015: Applied Cryptography: 10. Using Algorigthms: 10.1, 10.2, 10.3, 10.4

The article covers the following topics: 

### 10.1 CHOOSING AN ALGORITHM (summary)

The article explores the challenges of selecting a dependable algorithm for cryptography. While some may opt for a published algorithm or trust a manufacturer or consultant, or even write their own algorithm, each option carries certain risks. The author recommends choosing a public algorithm that has been evaluated by experts in the field. However, the author acknowledges that the cryptanalysis capabilities of military organizations may surpass those in the public domain. Moreover, algorithms intended for export from the US require NSA approval and are rumored to have built-in vulnerabilities. Consequently, selecting a public algorithm that has undergone rigorous scrutiny and cryptanalysis is the most prudent option.

### 10.2 PUBLIC-KEY CRYPTOGRAPHY VERSUS SYMMETRIC CRYPTOGRAPHY (summary)

The debate over which is better, public-key cryptography or symmetric cryptography, is based on a flawed assumption that the two can be compared equally. Needham and Schroeder argued that symmetric cryptography is more efficient than public-key cryptography due to the higher number and length of messages involved in public-key algorithms. However, this analysis overlooks the significant security benefits of public-key cryptography, which can handle tasks that symmetric cryptography cannot. Public-key cryptography is best suited for key management and a variety of protocols, while symmetric cryptography is ideal for encrypting data. Both have different properties and are used for different purposes, along with other primitives such as one-way hash functions and message authentication codes. Therefore, it is not a matter of which is better, but rather which is more appropriate for the specific task at hand.

### 10.3 ENCRYPTING COMMUNICATIONS CHANNELS (summary)

The article discusses how encryption can be used to secure communication channels between Alice and Bob. Encryption can take place at any layer of the OSI model, but in practice, it usually takes place at either the lowest layers or higher layers. The easiest place to add encryption is at the physical layer, which is called link-by-link encryption. The physical layer is standardized, and hardware encryption devices can be easily connected. However, every physical link in the network needs to be encrypted, which may become prohibitively expensive. Additionally, every node in the network must be protected, which is not always feasible. Despite these challenges, link-by-link encryption is effective, as a cryptanalyst cannot get any information about the structure of the information being communicated. Key management is also simple, as only the two endpoints of the line need a common key, and they can change their key independently from the rest of the network.

In summary, encryption is a powerful tool for securing communication channels, but the implementation details depend on the specific circumstances of the network. Link-by-link encryption at the physical layer is effective but may be expensive and require significant effort to implement in large networks.

End-to-End Encryption involves placing encryption equipment between the network and transport layers to encrypt only the transport data units and avoid encryption/decryption problems at the physical layer. However, routing information for the data is not encrypted, allowing for traffic analysis. Encryption at higher layers of the communication architecture, like the applications layer, can be independent of the type of communication network used and interact with user software. Combining link-by-link and end-to-end encryption is the most effective way of securing a network. Key management for the two schemes can be separate. End-to-end encryption offers a higher secrecy level but requires a more complex key-management system, and traffic analysis is possible since routing information is not encrypted.

### 10.4 ENCRYPTING DATA FOR STORAGE (summary)

Encrypting data for storage is different from encrypting data in transit. The encryption key has the same value as the message but is smaller and can be easily lost, and may need to be securely stored for years. Cryptography can also convert large secrets into smaller ones, making them more vulnerable to being lost. Other problems with encrypting computer data for storage include the possibility of plaintext data existing elsewhere, smaller data sizes, and complicated key management procedures. Retrieving encrypted files may also be inefficient if the encrypted files are structured as records and fields. It is important to ensure that the unencrypted file is erased after encryption.

When encrypting a hard drive, one can either use a single key to encrypt all the data, which is less secure and doesn't allow multiple users to access parts of the drive, or encrypt each file with a different key, which requires users to remember multiple keys. The solution is to encrypt each file with a separate key and encrypt those keys with another key known by the users. Driver-level encryption maintains a logical drive on the user's machine with all data encrypted, while file-level encryption encrypts each file separately. Providing random access to an encrypted drive can be done by using a unique initialization vector for each sector, generating a pseudo-random block as large as one sector, using error-recovering modes like CBC and CFB, or using a block cipher with a large enough block size.

Sources: [Schneier 2015: Applied Cryptography](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/19_chap10.html#chap10)

## y) Choose a password manager - KeePassX

KeePassX encrypts all user data, including passwords, notes, and other metadata, using the AES and Twofish encryption algorithms. The encrypted data is stored in a password-protected database file that can only be accessed using the master password.

### What treaths does it protect against?

Some of the threats it protects against include:

+ Password theft: KeePassX encrypts passwords and stores them in an encrypted database, which makes it difficult for attackers to steal passwords.
+ Password reuse: KeePassX can generate unique, complex passwords for each account, which reduces the risk of password reuse.
+ Phishing: KeePassX can be configured to launch websites from within the application, which reduces the risk of falling victim to phishing attacks that redirect users to fake websites.

### What information is encrypted, what's not?

KeePassX encrypts all user data, including passwords, notes, and other metadata, using the AES and Twofish encryption algorithms. The encrypted data is stored in a password-protected database file that can only be accessed using the master password.

### What's the license? How would you describe license's effects or categorize it?

The license for KeePassX is the GNU General Public License (GPL) version 2.0. This is a free and open-source software license that allows users to modify and distribute the software as long as they adhere to the terms of the license. The GPL license requires that any modified versions of the software must also be released under the same license.

### Where is the data stored? If in "the cloud", which country / juristiction / which companies? If on local disk, where? How is the data protected?

The data stored in KeePassX is typically stored locally on the user's device. The encrypted database file can be stored on a local disk, USB drive, or other removable media. It can also be stored in cloud storage services such as Dropbox, Google Drive, or OneDrive. However, it is important to note that the security of the data stored in the cloud will depend on the security of the cloud service provider and the user's account security.

Sources: [KeePassX](https://keepassxc.org)

## a) Demonstrate the use of a password manager

KeePassX - you will need to open the database file (in my case the location of the kdbx file and its name is covered) and enter the password
<img width="791" alt="image" src="https://user-images.githubusercontent.com/90892301/221427436-be31b053-d9ad-4680-924b-a0cd22db1c1c.png">

Here is an example of my test database with a test key
<img width="791" alt="image" src="https://user-images.githubusercontent.com/90892301/221427583-a98828f2-a6df-4e53-b681-e6881d31f2da.png">

## b) Encrypt and decrypt a message - GPG Suite tool

I have followed these steps:

+ Install GPG on your computer if it's not already installed.
+ Open a terminal or command prompt.
+ Generate a new key pair by running the command: gpg --gen-key

<img width="563" alt="image" src="https://user-images.githubusercontent.com/90892301/221662673-1a043fce-20a2-4e9d-ab66-d95643322ea2.png">

+ Once the key pair is generated, you can list your keys by running the command: gpg --list-keys
+ To encrypt a message, use the command: gpg --encrypt --recipient <recipient name or email address> <file name>

 <img width="756" alt="image" src="https://user-images.githubusercontent.com/90892301/221667438-e6a7c902-c834-46b5-8e22-bac9e156e7cb.png">

 + GPG will encrypt the file and create a new file with the .gpg extension.
 
 <img width="977" alt="image" src="https://user-images.githubusercontent.com/90892301/221667083-f0dd9411-2f1e-462a-b4ba-2183e3abcda0.png">  

+ To decrypt the message, use the command: gpg --decrypt <encrypted file name>
 
 <img width="540" alt="image" src="https://user-images.githubusercontent.com/90892301/221667869-7a9edcca-3f0f-47e8-afaa-59f380b2f045.png">

 Sources: [GNUPG Manual](https://www.gnupg.org/gph/en/manual/x110.html)
  
