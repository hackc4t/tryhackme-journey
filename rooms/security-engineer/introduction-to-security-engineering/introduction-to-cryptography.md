# Section 3 — Introduction to Cryptography

**🔗 Link:** [TryHackMe — Introduction to Cryptography](https://tryhackme.com/room/cryptographyintro)

---

### 🧠 What this section covers
> Learn about encryption algorithms such as AES, Diffie-Hellman key exchange, hashing, PKI, and TLS.

---

### 📘 Content
- Introduction

  This room introduced basic cryptography concepts, including symmetric encryption (AES), asymmetric encryption (RSA), Diffie-Hellman Key Exchange, hashing, and PKI.

  Simple ciphers were explained:

  Caesar Cipher: A substitution cipher shifting letters by a fixed key between 1–25. Example: encrypting “TRY HACK ME” with key 3 gives “WUB KDFN PH.” It can be broken using brute force by trying all possible keys.

  Transposition Cipher: Rearranges the order of letters based on a key. Example: message letters are written by columns and read by rows according to a key, producing a ciphertext different from substitution.

  Mono-alphabetic substitution cipher: Each letter maps to a unique letter. Example key “xpatvrzyjhecsdikbfwunqgmol” maps ‘a’→‘x’, ‘b’→‘p’, etc. Despite a large keyspace, this cipher can be broken using letter frequency analysis and dictionary knowledge, showing it is insecure for confidential communication.

  Secure encryption requires that recovering the plaintext be computationally infeasible, i.e., cannot be solved in polynomial time for practical purposes.  



---

### 📝 Answer Needed  
> N/A

