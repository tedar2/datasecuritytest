# H3 Hash

## x) Read and summarize - Schneier 2015: Applied Cryptography: 10. Using Algorigthms: 10.1, 10.2, 10.3, 10.4

The article covers the following topics: 



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

