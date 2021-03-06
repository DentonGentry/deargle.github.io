---

title: Lab &ndash; Asymmetric Encryption
number: 3
---

<div class='alert alert-danger'><strong>Important:</strong> To receive full credit, you must complete Part 1 of the lab by the day marked in the calendar, which entails setting up GPG on your computer and sending Dr. Eargle your PGP public (not private) key. This is required for the PGP key signing class activity on Monday (marked in the calendar). Instructions for creating your PGP public key is described in the “Install PGP and Create a Public-Private Key Pair” section in this document.</div>

<div class='alert alert-info'>While some of the tools for this lab are installed on the lab VM, it's probably best if you install GPG onto your own laptop since you'll be configuring your personal email
and it might be nice to have access to that with the lab tools outside of class needs.</div>

# Part 1. Install PGP and Create a Public-Private Key Pair

In this section of the lab, you will generate a PGP public-private key pair. You can do this using a variety of software, including the free implementation of PGP, GPG. For Mac users, I recommend using Apple Mail and GPG Tools ([https://gpgtools.org](https://gpgtools.org)). For Windows users, I recommend Gpg4Win (not the Lite version; [http://www.gpg4win.org](http://www.gpg4win.org)) in conjunction with Outlook, Thunderbird, or Claw Mail. 

A setup guide for GPG Tools (for Mac users) is available at: 

[http://support.gpgtools.org/kb/how-to/first-steps-where-do-i-start-where-do-i-begin](http://support.gpgtools.org/kb/how-to/first-steps-where-do-i-start-where-do-i-begin)

A setup guide for Gpg4Win (Windows users) is available at:

[http://www.gpg4win.org/doc/en/gpg4win-compendium_11.html](http://www.gpg4win.org/doc/en/gpg4win-compendium_11.html)

[https://www.gpg4win.org/doc/en/gpg4win-compendium_12.html](https://www.gpg4win.org/doc/en/gpg4win-compendium_12.html)

(if you're using the lab vm, you can skip to the second link).

Save/export your generated key in a text file with the extension “.asc” and email this file to Dr. Eargle. With gpg4win's Kleopatra, do this by clicking “Create a backup of your key pair,” and make sure to select the ASCII armor option.

**Important:** [To better future-proof your key](https://www.yubico.com/2015/02/big-debate-2048-4096-yubicos-stand/), Generate a 4096-bit key, not the default 2048-bit one. 

Make sure that your public key includes all of the email addresses you want to send and receive encrypted messages with. Finally, make sure that you include your first and last name so that people can look up your public key on a key server like pgp.mit.edu.

Important: You should end up with a .asc file that contains the following string at the top of the file: 

`-----BEGIN PGP PUBLIC KEY BLOCK-----`

If instead your .ASC file contains the string:

`-----BEGIN PGP PRIVATE KEY BLOCK-----`

<span class='label label-danger'>Then is the wrong key. Do NOT send this private key to Dr. Eargle.</span>

Finally, record your PGP fingerprint below. For example, Dr. Eargle’s PGP fingerprint is [on his homepage](https://daveeargle.com).

**Your PGP fingerprint:**



## Part 2. Understanding Asymmetric Cryptography

Note: To help you answer the questions in this section, view this “RSA Algorithm” video:

[https://youtu.be/Z8M2BTscoD4](https://youtu.be/Z8M2BTscoD4).

### Key Exchange Problem

1. Imagine 200 people wish to communicate securely using symmetric keys, one symmetric key for each pair of people. How many symmetric keys would this system use in total? (See [http://en.wikipedia.org/wiki/Metcalf%27s_law](http://en.wikipedia.org/wiki/Metcalf%27s_law)). 

    **Answer:**

2. Does a 256-bit RSA key (a key with a 256-bit modulus) provide strength similar to that of a 256-bit AES key? Explain. Note: This site gives estimates for good key lengths: 

    [http://www.keylength.com](http://www.keylength.com)
	
	Help interpreting this site: If you were to select "Compare all methods", and then enter the year "2030", the “Method” column means “group that makes recommendations using their method” (recall that NIST held the competition that resulted in the AES winner being selected). “Date” means how long you’ll be secure until. “Symmetric” means the minimum keysize you would need to be secure for that long using a symmetric method such as AES. “Factoring Modulus” means the minimum keysize you would need to be secure for that long using an asymmetric method such as RSA. 

	**Answer:** 

3. Complete encryption and decryption using the RSA algorithm, for the following data (show all work): `p = 5, q = 11, e = 3, M = 9`. See the “RSA Algorithm” video link above. Also:

    [http://en.wikipedia.org/wiki/RSA_(cryptosystem)](http://en.wikipedia.org/wiki/RSA_(cryptosystem))

	**Answer:**

4. In a public-key system using RSA, you intercept the ciphertext, `C=10`, sent to a user whose public key is `e=5, n=35`.  What is the plaintext `M`?

	**Answer:**

