# Encryption

## Cryptography

The process of transforming information into a form (ciphertext) that unintended readers can't understand\
One of the main security controls used to protect information online\
**Cipher** is a algorithm that encrypts/decrypts information
- Caesar's cipher is one of the earliest cryptography used
- Simple algorithm that works by shifting letters in the Roman alphabet forward by a fixed number of spaces
- The shifting number is the key to encrypt/decrypt information

Every form of encryption relies on both a cipher and key to secure the exchange of information

#### Symmetric-encryption

- Only one key is used
- All parties involved use the same key to encrypt/decrypt information
- Faster to process
- Ciphertext size is about the same size as the original text
- Usually uses 128-bits or 256-bits key
- Algorithms
  - QUAD
  - DES
  - 3DES
  - RC4
  - AES

![img](https://sectigostore.com/blog/wp-content/uploads/2020/04/types-of-encryption-symmetric-encryption.png)

#### Asymmetric-encryption

- The use of a *public* and *private* key pair for encryption and decryption of data
- Slower to process
- Ciphertext is bigger than the original text
- The keys are at least 100-bits long
- Algorithms
- Diffie-Hellman
- ECC
- DSA
- RSA

![img](https://sectigostore.com/blog/wp-content/uploads/2020/04/types-of-encryption-asymmetric-encryption.png)

## Public Key Infrastructure (PKI)

An encryption framework that secures the exchange of information online\
Broad system that makes accessing information fast, easy and secure

### How PKI works

- Two-step process
  - Starts with the exchange of encrypted information
    - Involves either [asymmetric](#asymmetric-encryption)/[symmetric](#symmetric-encryption) encryption or both
  - Establish trust using a system of digital certificates
    - Digital certificate: A file that verifies the identity of a public key holder

## Hashing

### Hash function

An algorithm that produces a code that can't be decrypted\
Hashing algorithms produce a unique identifier known as a hash value, or digest\

- Hashes are primarily used as a way to determine the *integrity* of files and applications
- Data integrity relates to the accuracy and consistency of information AKA non-repudiation

### Hash collisions

When hash fuction outputs same hash values for different inputs\
Hash algorithms map any input, regardless of its length, into a fixed-size value (finite set of available outputs)

### Rainbow tables

A file of pre-generated hash values and their associated planetext\
Attackers can obtain password hash and use Rainbow table to compare them against all possible values

### Salting

An additional safeguard that's used to strengthen hash fuctions
- *salt* is a random string of characters that's added to the data before it's hashed
- salting produces a more unique hash value, making salted data resilient to rainbow table attacks
