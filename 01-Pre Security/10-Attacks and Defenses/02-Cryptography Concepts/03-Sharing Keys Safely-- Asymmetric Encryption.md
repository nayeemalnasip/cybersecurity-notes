# Cryptography

## Asymmetric Encryption

### Overview

Asymmetric encryption is a cryptographic technique designed to solve one of the biggest challenges in symmetric encryption: securely sharing encryption keys over an untrusted network. Instead of using a single shared key, asymmetric encryption uses a pair of mathematically related keys—a public key and a private key.

This technology forms the foundation of secure web browsing, digital certificates, secure email systems, VPNs, digital signatures, and modern authentication systems.

---

## Main Concept

### What is Asymmetric Encryption?

Asymmetric encryption, also known as **Public Key Cryptography (PKC)**, uses two separate keys:

* **Public Key** → Shared openly with anyone.
* **Private Key** → Kept secret by the owner.

The two keys are mathematically linked, but deriving the private key from the public key is computationally impractical.

### Core Principle

```text
Public Key → Encrypt Data

Private Key → Decrypt Data
```

Only the owner of the private key can decrypt data encrypted with the corresponding public key.

---

## How It Works

### Step 1: Generate Key Pair

Bob generates two keys:

```text
Public Key
Private Key
```

---

### Step 2: Share the Public Key

Bob distributes his public key publicly.

Examples:

* Website
* Email Signature
* Certificate Server
* Public Key Repository

The public key is not considered secret.

---

### Step 3: Encrypt Data

Alice wants to send a confidential message.

```text
Plaintext:
HELLO BOB
```

Alice encrypts the message using Bob's public key.

```text
Public Key + Plaintext
        ↓
Ciphertext
```

---

### Step 4: Send Ciphertext

The encrypted message travels through the internet.

Even if intercepted, it cannot be read without Bob's private key.

---

### Step 5: Decrypt Data

Bob receives the ciphertext and decrypts it.

```text
Ciphertext + Private Key
            ↓
         Plaintext
```

Result:

```text
HELLO BOB
```

---

## Important Components

### Public Key

A publicly available key used for encryption.

Characteristics:

* Can be shared openly.
* Used to encrypt data.
* Does not need confidentiality.

Example:

```text
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8A
-----END PUBLIC KEY-----
```

---

### Private Key

A secret key owned by a single individual or system.

Characteristics:

* Must never be shared.
* Used for decryption.
* Compromise leads to loss of security.

Example:

```text
-----BEGIN PRIVATE KEY-----
MIIEvQIBADANBgkqhkiG9w0BAQEFAAS
-----END PRIVATE KEY-----
```

---

### Key Pair

The public and private keys are generated together.

| Component   | Purpose    |
| ----------- | ---------- |
| Public Key  | Encryption |
| Private Key | Decryption |

---

### Ciphertext

Encrypted data generated after applying the public key.

Example:

```text
4F2A8B91C7D5F8...
```

Without the corresponding private key, recovering the original message is extremely difficult.

---

## The Mailbox Analogy

Asymmetric encryption can be compared to a public mailbox.

| Mailbox Component | Cryptography Equivalent |
| ----------------- | ----------------------- |
| Mail Slot         | Public Key              |
| Locked Door       | Private Key             |
| Letter            | Plaintext               |
| Stored Mail       | Ciphertext              |

### Process

1. Anyone can place a letter through the mail slot.
2. Only the mailbox owner can open the locked door.
3. The owner retrieves and reads the letters.

Similarly:

* Anyone can encrypt data using a public key.
* Only the private key owner can decrypt it.

---

## Solving the Key Distribution Problem

### Problem in Symmetric Encryption

```text
Alice ↔ Bob

Need Shared Secret Key
```

Question:

```text
How do they safely exchange the key?
```

If the key is intercepted:

```text
Attacker obtains key
↓
Attacker decrypts traffic
```

Security is lost.

---

### Solution with Asymmetric Encryption

```text
Bob generates:
    Public Key
    Private Key

Bob publishes:
    Public Key

Bob protects:
    Private Key
```

Alice simply downloads Bob's public key and encrypts her message.

No secret key needs to be exchanged beforehand.

This solves the key distribution problem.

---

## Digital Certificates

### What is a Certificate?

A digital certificate is an electronic document that proves ownership of a public key.

Certificates help verify that a public key actually belongs to the claimed website or organization.

---

### Certificate Contents

| Field             | Description                  |
| ----------------- | ---------------------------- |
| Subject           | Website or Organization Name |
| Public Key        | Public Encryption Key        |
| Issuer            | Certificate Authority        |
| Valid From        | Start Date                   |
| Valid Until       | Expiration Date              |
| Digital Signature | Verification Signature       |

---

### Example

```text
Issued To:
www.example.com

Issued By:
Trusted Certificate Authority

Valid Until:
31-Dec-2027
```

---

## Certificate Authorities (CA)

### What is a CA?

A Certificate Authority is a trusted organization that verifies identities and signs certificates.

Examples:

* DigiCert
* Sectigo
* GlobalSign
* Let's Encrypt

### Responsibilities

* Verify domain ownership.
* Issue certificates.
* Sign certificates digitally.
* Revoke compromised certificates.

---

## HTTPS and Asymmetric Encryption

### Secure Website Connection Process

When visiting:

```text
https://example.com
```

The following occurs:

### Step 1

Browser requests the website.

---

### Step 2

Website sends:

```text
Digital Certificate
+
Public Key
```

---

### Step 3

Browser verifies:

* Certificate validity
* Trusted CA signature
* Expiration date
* Domain ownership

---

### Step 4

Browser and server establish a shared secret key.

This process uses asymmetric encryption.

---

### Step 5

Session switches to symmetric encryption.

Algorithms commonly used:

```text
AES-128
AES-256
ChaCha20
```

---

### Why Switch?

Asymmetric encryption is secure but computationally expensive.

Symmetric encryption is much faster for ongoing communication.

---

## Hybrid Encryption Model

Modern systems combine both encryption methods.

### Initial Connection

```text
Asymmetric Encryption
```

Purpose:

```text
Secure Key Exchange
```

---

### Data Transfer

```text
Symmetric Encryption
```

Purpose:

```text
Fast Data Encryption
```

---

### Used In

* HTTPS/TLS
* VPNs
* Secure Messaging Applications
* Cloud Platforms
* Online Banking

---

## Symmetric vs Asymmetric Encryption

| Feature             | Symmetric Encryption | Asymmetric Encryption  |
| ------------------- | -------------------- | ---------------------- |
| Keys Used           | One Shared Key       | Public + Private Key   |
| Encryption Speed    | Fast                 | Slower                 |
| Key Sharing         | Difficult            | Easy                   |
| Main Purpose        | Bulk Data Encryption | Secure Key Exchange    |
| Security Dependency | Shared Secret Key    | Private Key Protection |
| Example Algorithms  | AES, DES, 3DES       | RSA, ECC               |

---

## Advantages / Benefits

### Secure Key Distribution

Eliminates the need to secretly exchange keys.

### Authentication

Helps verify identities through certificates.

### Scalability

Public keys can be distributed globally.

### Digital Trust

Enables trusted online communication.

### Foundation of HTTPS

Provides secure web browsing and online transactions.

---

## Key Characteristics

* Uses two mathematically related keys.
* Public key can be shared openly.
* Private key must remain secret.
* Solves the key distribution problem.
* Slower than symmetric encryption.
* Commonly used for authentication and key exchange.
* Supports digital certificates and HTTPS.
* Forms the basis of modern internet security.

---

## Example

### Secure Website Connection

A user visits:

```text
https://www.example.com
```

Process:

1. Server sends its certificate and public key.
2. Browser verifies the certificate.
3. Browser establishes a shared secret securely.
4. Both parties switch to AES encryption.
5. User securely browses the website.

Result:

```text
Confidentiality
Integrity
Authentication
```

---

## Key Notes

* Asymmetric encryption uses two keys.
* Public keys can be distributed publicly.
* Private keys must remain secret.
* Public Key Cryptography solves the key distribution problem.
* HTTPS relies on asymmetric encryption during connection setup.
* Certificates verify public key ownership.
* Certificate Authorities issue trusted certificates.
* Real-world systems use hybrid encryption.
* Asymmetric encryption is slower but more flexible.
* Symmetric encryption is faster and handles bulk data transfer.

---

## Learning Outcome

After completing this section, I understood how asymmetric encryption solves the key distribution problem using public and private key pairs. I learned how public keys enable secure communication without sharing secret keys, how digital certificates and Certificate Authorities establish trust, and how modern technologies such as HTTPS combine asymmetric and symmetric encryption to provide secure, authenticated, and efficient communication across the internet.
