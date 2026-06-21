# Cryptography

## Cryptography Fundamentals Summary

### Overview

Cryptography is a fundamental cybersecurity discipline that protects sensitive information from unauthorized access and modification. It supports two critical pillars of the CIA Triad—**Confidentiality** and **Integrity**—by ensuring that data remains private and trustworthy during storage and transmission.

Modern cybersecurity relies heavily on cryptographic technologies to secure websites, online banking, cloud services, email communications, VPNs, and digital identities.

---

## Main Concept

### What is Cryptography?

Cryptography is the science of protecting information through mathematical techniques that transform readable data into an unreadable format.

The primary goal is to ensure that only authorized individuals can access or verify information.

### Core Security Objectives

| Objective       | Description                                 |
| --------------- | ------------------------------------------- |
| Confidentiality | Prevent unauthorized access to data         |
| Integrity       | Detect unauthorized modification of data    |
| Authentication  | Verify the identity of users and systems    |
| Non-Repudiation | Prevent denial of actions or communications |

---

## How It Works

### Basic Cryptographic Process

#### Step 1: Plaintext

Original readable information.

```text
Patient Name: Alice Smith
```

#### Step 2: Encryption

An algorithm and key transform the data.

```text
Plaintext + Key + Algorithm
```

#### Step 3: Ciphertext

Encrypted unreadable data.

```text
8F3A91B7D2F84C...
```

#### Step 4: Transmission

The ciphertext travels through networks.

#### Step 5: Decryption

The authorized recipient restores the original message using the appropriate key.

```text
Ciphertext + Key
↓
Plaintext
```

---

## Important Components

### Plaintext

Readable data before encryption.

Examples:

```text
HELLO
Password123
Medical Records
```

---

### Ciphertext

Encrypted data designed to appear meaningless.

Examples:

```text
KHOOR
8F3A91B7D24F...
```

---

### Cryptographic Key

A secret value that controls encryption and decryption operations.

Characteristics:

* Must remain confidential
* Determines cryptographic strength
* Essential for secure communication

---

### Algorithm

A publicly known mathematical procedure used to encrypt and decrypt information.

Examples:

| Algorithm Type | Examples         |
| -------------- | ---------------- |
| Symmetric      | AES, DES, 3DES   |
| Asymmetric     | RSA, ECC         |
| Hashing        | SHA-256, SHA-512 |

---

## Encryption Methods

### Symmetric Encryption

Uses a single shared key.

```text
Encryption Key = Decryption Key
```

#### Characteristics

* Fast
* Efficient
* Suitable for large volumes of data

#### Examples

```text
AES
DES
3DES
```

#### Challenge

```text
Key Distribution Problem
```

Securely sharing the secret key between parties can be difficult.

---

### Asymmetric Encryption

Uses two mathematically linked keys.

```text
Public Key
Private Key
```

#### Characteristics

* Solves key distribution challenges
* Supports authentication
* Enables secure communication between strangers

#### Examples

```text
RSA
ECC
```

#### Key Principle

```text
Public Key → Encrypt

Private Key → Decrypt
```

---

## Hybrid Encryption Model

Modern systems combine both encryption methods.

### Phase 1: Secure Key Exchange

Uses:

```text
Asymmetric Encryption
```

Purpose:

```text
Securely establish a shared secret
```

---

### Phase 2: Data Protection

Uses:

```text
Symmetric Encryption
```

Purpose:

```text
Fast and efficient data encryption
```

---

### Real-World Technologies

* HTTPS
* TLS
* VPNs
* Secure Messaging Applications
* Online Banking Platforms
* Cloud Services

---

## Certificates and Trust

### Digital Certificates

Certificates verify the ownership of public keys.

Certificate information includes:

| Field           | Description            |
| --------------- | ---------------------- |
| Subject         | Domain or Organization |
| Public Key      | Encryption Key         |
| Issuer          | Certificate Authority  |
| Validity Period | Expiration Dates       |
| Signature       | Trust Verification     |

---

### Certificate Authorities (CA)

Trusted organizations responsible for issuing and validating certificates.

Examples include:

* Let's Encrypt
* DigiCert
* Sectigo
* GlobalSign

---

## Advantages / Benefits

### Data Confidentiality

Protects sensitive information from unauthorized access.

### Data Integrity

Detects unauthorized modification of information.

### Secure Communication

Protects information while it travels across networks.

### Authentication

Verifies the identity of users, websites, and systems.

### Scalability

Supports secure communication on a global scale.

### Foundation of Internet Security

Enables secure web browsing, online payments, and digital services.

---

## Key Characteristics

* Cryptography protects confidentiality and integrity.
* Plaintext is readable information.
* Ciphertext is encrypted information.
* Algorithms define how encryption operates.
* Keys control encryption and decryption.
* Symmetric encryption uses one shared key.
* Asymmetric encryption uses public and private keys.
* HTTPS uses both encryption methods together.
* Certificates establish trust between users and websites.
* Modern internet security relies heavily on cryptographic technologies.

---

## Example

### Secure Website Connection

When a user visits:

```text
https://example.com
```

The following occurs:

1. The website provides its certificate and public key.
2. The browser verifies the certificate.
3. A secure session key is established using asymmetric encryption.
4. Symmetric encryption secures all subsequent communication.
5. The browser displays the padlock icon.

Result:

```text
Secure
Authenticated
Encrypted Communication
```

---

## Key Notes

* Cryptography protects confidentiality and integrity.
* Plaintext is readable data.
* Ciphertext is encrypted data.
* Security depends on protecting cryptographic keys.
* Symmetric encryption is fast but requires secure key sharing.
* Asymmetric encryption solves the key distribution problem.
* Digital certificates verify public key ownership.
* Certificate Authorities establish trust.
* HTTPS uses a hybrid cryptographic model.
* Cryptography is a critical component of modern cybersecurity.

---

## Learning Outcome

After completing this room, I understood the fundamental principles of cryptography and its role in protecting confidentiality and integrity within the CIA Triad. I learned the differences between plaintext and ciphertext, the importance of cryptographic keys and algorithms, the operation of symmetric and asymmetric encryption, the key distribution problem, and the role of certificates and Certificate Authorities in establishing trust. I also gained an understanding of how modern technologies such as HTTPS combine both encryption methods to provide secure, authenticated, and efficient communication across the internet.
