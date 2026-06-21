When you see the padlock icon (HTTPS) in your browser, the main thing protecting your data is cryptography — specifically TLS (Transport Layer Security), which encrypts the connection between your device and the website.

This means that even if someone intercepts the traffic, they should not be able to read or modify it without the proper cryptographic keys.

### Cryptography — Study Note

### Overview

Cryptography is the practice of protecting information using mathematical techniques. It helps ensure that data remains confidential (secret), intact (unchanged), and authentic (from the real sender).

It is one of the most important foundations of modern cybersecurity and is used in:

* HTTPS websites

* Online banking

* Messaging apps

* VPNs

* Cloud services

* Digital signatures

### Main Concept

### What is Cryptography?

Cryptography converts readable information into an unreadable form so that only authorized people can access it.

Readable Data (Plaintext)

Encryption

Unreadable Data (Ciphertext)

Decryption with Correct Key

Original Plaintext Restored

### How It Works

### Step-by-Step Process

1. Plaintext — Original readable message.

2. Algorithm — Mathematical method used for encryption.

3. Key — Secret value that controls the encryption process.

4. Encryption — Plaintext is transformed into ciphertext.

5. Transmission — Ciphertext travels across the network.

6. Decryption — The recipient uses the correct key to recover the original message.

### Important Components

### Plaintext vs Ciphertext

| Type       | Example           |
| ---------- | ----------------- |
| Plaintext  | Patient: John Doe |
| Ciphertext | 8F3A91B7C2...     |

### Algorithms

Common cryptographic algorithms include:

| Algorithm | Purpose                        |
| --------- | ------------------------------ |
| AES       | Symmetric encryption           |
| RSA       | Asymmetric encryption          |
| ECC       | Modern public-key cryptography |
| SHA-256   | Hashing (integrity)            |

### Keys

Keys are critical because the algorithm may be public, but the key must remain secret.

### Key Principle

If an attacker gets the key, they can usually decrypt the data.

### Types of Encryption

### 1. Symmetric Encryption

One key is used for both encryption and decryption.

![PPT - Cryptography Introduction PowerPoint Presentation, free download - ID:2392175](https://images.openai.com/static-rsc-4/aA7iaHtnJh0tv5I4FKmq0PItFNkKF1BOJycXEBLgrunEG32vl8LIejLV9FsnMLW-OQ1Cp2e0n4zhLnOvTSvqC88wcuLSPw5Qs08M1cNfjZqo0wO0QNuvIY0aWClUuvbWniuyuKKpKbx8tlPXLyF8ybBeVA4DVjYyEKgY6NmNTW-mCYyjd2MnQME5gVIkXAop?purpose=fullsize)

### Analogy

Think of a lockbox where both people share the same key.

### Advantages

* Very fast

* Efficient for large amounts of data

* Used in HTTPS data transfer

### Disadvantage

* The secret key must be shared securely.

### 2. Asymmetric Encryption

Uses two different keys:

* Public Key — Can be shared with everyone.

* Private Key — Must remain secret.

![Symmetric vs. Asymmetric Encryption Explained - DEV Community](https://images.openai.com/static-rsc-4/vF69kU3u35dqt_tUGgwdiy_Zxp1eJsvezDEjT5pH9J_KXr1UVfeR5xBbl4AsIWN24eIFnBeWJu1fpFIe-8BARC5QeXeHvRjNoCeD5oznUg4T_-11gFpu_LKs1Ex_Drce6G810CP4zBPgZ9q_NDePLu_f0pqn9QKqj8Rn65jujzBCEY1JVbd_3xZwB8A4Jt3g?purpose=fullsize)

### Analogy

A mailbox:

* Anyone can put a letter in (public key).

* Only the owner can open it (private key).

### Advantages

* Solves the key-sharing problem.

* Enables digital signatures.

### Disadvantage

* Slower than symmetric encryption.

### How HTTPS Uses Both

![One moment, please...](https://images.openai.com/static-rsc-4/UXsVR5So8VVLwUHYKIbzIhnVM4B-y81VlPpJoggEv0dB6VLlkSGcOJBJYTdQpHQ1-O9BR7C-4GisR_zHDZufz49AgAF_Jd2Z_qLfup4snFEbvQE6McSUdrYgP1QwnjBvwBnxxWpYIvB9ufuQSBT6NSjiWBy18oOi21Gf60Y6zgMSuZiDTDzpbgnr7caNFNHe?purpose=fullsize)

When you visit a secure website:

1. Your browser gets the website's public key.

2. It securely exchanges a temporary symmetric key.

3. After that, both sides use fast symmetric encryption (AES) for the actual data.

### This is what the padlock icon represents.

Your browser has established an encrypted connection using TLS.

### Advantages / Benefits

* Protects sensitive information.

* Prevents eavesdropping.

* Detects tampering.

* Verifies identities.

* Enables secure online transactions.

* Protects passwords and personal data.

### Key Characteristics

* Confidentiality — Keeps data secret.

* Integrity — Detects modifications.

* Authentication — Verifies who is communicating.

* Non-repudiation — Helps prove who sent a message.

### Real-World Example

### Medical Clinic Scenario

Healthcare

A clinic sends patient records to a specialist.

Without cryptography: Anyone on the network could read or alter the records.

With cryptography:

* The records are encrypted.

* Only the specialist can decrypt them.

* Any tampering can be detected.

### Key Notes (Exam Revision)

Plaintext = readable data.

Ciphertext = encrypted unreadable data.

Encryption converts plaintext to ciphertext.

Decryption restores the original data.

Symmetric encryption uses one shared key.

Asymmetric encryption uses public and private keys.

HTTPS/TLS combines both methods.

The browser padlock indicates a TLS-encrypted connection.

### Learning Outcome

After completing this section, I understood how cryptography protects confidentiality and integrity, the difference between plaintext and ciphertext, the role of algorithms and keys, and how symmetric and asymmetric encryption work together to secure modern web browsing through HTTPS and TLS.
