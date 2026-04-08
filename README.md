# MD5 vs SHA-256 in Kali Linux

## Overview
This project demonstrates the practical use of cryptographic hash functions in Kali Linux, focusing on MD5 and SHA-256.

The project also connects the practical lab execution to theoretical concepts of:
- Determinism  
- Fixed-length output  
- Avalanche effect  
- Algorithm strength  
- Security implications of legacy hashing algorithms  

---

## Objectives
The main objectives of this lab were to:
1. Generate MD5 hashes for selected plaintext values in Kali Linux  
2. Generate SHA-256 hashes for the same plaintext values  
3. Observe how input changes affect the resulting digest  
4. Compare the security relevance of MD5 and SHA-256  
5. Support academic concepts with real command-line evidence  

---

## Tools and Environment
- **Operating System:** Kali Linux  
- **Shell:** Bash  
- **Commands Used:** `md5sum`, `sha256sum`  

---

## MD5 Hash Generation
```bash
echo -n "Password123" | md5sum
echo -n "Cyber123" | md5sum
echo -n "N3Tw0rkLa6" | md5sum
⚙️ SHA-256 Hash Generation
echo -n "Password123" | sha256sum
echo -n "Cyber123" | sha256sum
echo -n "N3Tw0rkLa6" | sha256sum
echo -n "N3Tw0rkLa6_2026" | sha256sum

Note: The -n flag prevents adding a newline character.

📊 Results

MD5 Hash Outputs
Input	MD5 Hash
Password123	42f749ade7f9e195bf475f37a44cafcb
Cyber123	9e8500ad4487d091b08d3b0e32978cb8
N3Tw0rkLa6	2f19d49882064cb6bc5d5aa4ae9b05ec

SHA-256 Hash Outputs
Input	SHA-256 Hash
Password123	008c70392e3abfbd0fa47bbc2ed96aa99bd49e159727fcba0f2e6abeb3a9d601
Cyber123	185160cde4162679eac934d1f307db6a3c4510e1bd9ba106f77cbd25852dcc22
N3Tw0rkLa6	e68a03f62270cdee6434b63b958739d1cdc89117ec74da49bf7d816312e4c7ce
N3Tw0rkLa6_2026	9b9f7c49c2c71516692fbb39634eb673a287959eae4fcb725283163e456c1485

Key Observations
Same input always produces the same hash (determinism)
Output length remains constant regardless of input size
Small input changes create completely different hashes (avalanche effect)
MD5 is fast but insecure
SHA-256 is stronger and widely used

Security Analysis
MD5 Weaknesses
Vulnerable to collision attacks
Can be cracked using rainbow tables
Fast computation enables brute-force attacks
SHA-256 Strengths
Strong collision resistance
Used in modern security systems (TLS, blockchain, etc.)
Remains secure under current standards

Note: For password storage, modern systems use bcrypt, scrypt, or Argon2 instead of basic hashing.

Lab Execution Screenshots

MD5 Execution

Figure 1: MD5 Hash of Password123 (figure1-md5-password123.png)


Figure 2: MD5 Hash of Cyber123 (figure2-md5-cyber123.png)


Figure 3: MD5 Hash of N3Tw0rkLa6 (figure3-md5-n3tworkla6.png)


SHA-256 Execution

Figure 4: SHA-256 Hash of Password123 (figure4-sha256-password123.png)


Figure 5: SHA-256 Hash of Cyber123 (figure5-sha256-cyber123.png)


Figure 6: SHA-256 Hash of N3Tw0rkLa6 (figure6-sha256-n3tworkla6.png)


Figure 7: SHA-256 Hash of N3Tw0rkLa6_2026 (figure7-sha256-n3tworkla6-2026.png)


Repository Structure

README.md
images/
report/