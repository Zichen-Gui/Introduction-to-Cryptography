# CSCI 4900/6900 Introduction to Cryptography
Welcome to the course repository of CSCI 4900/6900 Introduction to Cryptography! You can find an overview of the course below (updated weekly). The programming exercises of the course are in the `Labs` folder.


## Lectures
| Lecture | Topic(s)                                                                                                                                             | Remarks             |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| 1       | - History of cryptography <br> - Aim of modern cryptography <br> - Shannon Cipher and perfect security <br> - Computational ciphers and semantic security (informal) | - Boneh&Shoup 2.1     |
| 2       | - Semantic security (formal) <br> - Why should everyone care about cryptography? | - Boneh&Shoup 2.2 <br> - [Sudheendra Raghav Neela. The Workings of WhatsApp’s Backups (and Why You Should Enable End-to-End Encrypted Backups)](https://snee.la/posts/the-workings-of-whatsapps-end-to-end-encrypted-backups/) <br> - [Daniel J. Solove. 'I've Got Nothing to Hide' and Other Misunderstandings of Privacy.](https://scholarship.law.gwu.edu/faculty_publications/158/)   |
| 3       | - Pseudorandom generators (PRGs) <br> - Limitation of stream cipher (built from PRGs) <br> - Parallel composition of PRGs | - Boneh&Shoup 3.1-3.4 |
| 4       | - Sequential composition of PRGs (the Blum-Micali construction) <br> - The subset sum generator <br> - The Salsa and Chacha PRGs | - Boneh&Shoup 3.4, 3.6, 3.7.2 |
| 5       | - Linear congruential generator <br> - The Content Scrambling System (CSS) <br> - Pseudorandom Number Generator (PRNG) <br> - Generating random bits in practice | - Boneh&Shoup 3.7.1, 3.8, 3.10 <br> -  [Massimiliano Taverna and Kenneth G. Paterson. Snapping Snap Sync: Practical Attacks on Go Ethereum Synchronising Nodes.](https://www.usenix.org/conference/usenixsecurity23/presentation/taverna)|
| 6       | - Block Cipher <br> - DES/Double-DES/Triple-DES <br> - AES (do not implement your own primitive!) <br> - Pseudorandom function | - Boneh&Shoup 4.1, 4.2, 4.4 <br> - [Ping Wang, Shishir Nagaraja, Aurelien Bourquard, Haichang Gao and Jeff Yan. SoK: Acoustic Side Channels.](https://arxiv.org/abs/2308.03806) <br> - [Computerphile (Presented by Mike Pound, original paper by Nassi et al.). Power LED Attack.](https://www.youtube.com/watch?v=vXe8pe18MNk) |
| 7       | - PRF Switching Lemma <br> - Constructing PRGs from PRFs <br> - Deterministic counter mode <br> - Constructing block ciphers from PRFs <br> - Constructing PRFs from PRGs | - Boneh&Shoup 4.4, 4.5, 4.6 |
| 8       | - Semantic security against chosen plaintext attack (CPA) <br> - ECB and deterministic counter modes are not secure against CPA <br> - Generic hybrid construction <br> - Randomized counter mode <br> - Randomized CBC mode | - Boneh&Shoup 5.1-5.4 <br> - [Code-breaking before the Battle of Midway](https://en.wikipedia.org/wiki/Battle_of_Midway#U.S._code-breaking) |
| 9       | - Nonce-based encryption <br> - Encrypted search <br> - Message Authentication Code (MAC) | - Boneh&Shoup 5.5, 6.1 <br> - [Dawn Xiaoding Song, D. Wagner and A. Perrig. Practical techniques for searches on encrypted data.](https://ieeexplore.ieee.org/document/848445) <br> - [Client-Side Field Level Encryption from MongoDB](https://www.mongodb.com/docs/manual/core/csfle/reference/supported-operations/#supported-query-operators) <br> - [Marketing of Blind Insight (FAQ 02: We use AES and we can do real-time search at the same time!)](https://www.blindinsight.com/product) <br> - [Muhammad Naveed, Seny Kamara, and Charles V. Wright. Inference Attacks on Property-Preserving Encrypted Databases.](https://dl.acm.org/doi/10.1145/2810103.2813651)|
| 10      | - Security notion of MAC (sEUF-CMA) <br> - Verification queries do not help the adversary <br> - Constructing MACs from PRFs <br> - CBC prefix-free secure PRF <br> - Cascade prefix-free PRF <br> - Encrypted MAC (ECBC and NMAC) | - Boneh&Shoup 6.1-6.5  |
| 11      | - Prefix-free encodings <br> - Randomized $\varepsilon$-prefix-free encoding and CMAC <br> - Converting a block-wise PRF to bit-wise PRF <br> - ANSI CBC-MAC, CMAC and (simplified) PMAC <br> - Using the same key for encryption and MAC: ciphertext and tag forgery on CBC encryption + (raw) CBC-MAC | - Boneh&Shoup 6.6-6.11 <br> - [Prefix code](https://en.wikipedia.org/wiki/Prefix_code) <br> - [Elias gamma coding](https://en.wikipedia.org/wiki/Elias_gamma_coding) (The version I introduced ($0^{\vert m \vert} \mathbin\Vert 1 \mathbin\Vert m$ for number $m$ represented as a binary string) is more intuitive but it is not the shortest way to encode a number using this method. The version you see on Wikipedia is shorter by 2 bits.) |
| 12      | - Universal hash functions <br> - Security of universal hash functions <br> - The CBC and cascading constructions are computational UHFs (computationally secure) <br> - UHFs using polynomials (statistically secure) | - Boneh&Shoup 7.1-7.2  |
| 13      | - UHFs using polynomials <br> - A parallel UHF from a small PRF <br> - PRF(UHF) composition | - Boneh&Shoup 7.2-7.3  |
| 14      | - The Carter-Wegman MAC <br> - Difference unpredictable functions (DUFs) <br> - One-time MAC | - Boneh&Shoup 7.4,7.6  |



## Labs
| Lab | Topic(s)                                       | Remarks |
|-----|------------------------------------------------|---------|
| 1   | - Implement One-Time Pad <br> - Attack Two-Time Pad |         |
| 2   | - Attack `Math.random()` in Java 8 <br> - Implement the Content Scrambling System (CSS). <br> - Attack CSS |         |
| 3   | - Implement FEAL <br> - Attack FEAL | -  [Akihiro Shimizu, Shoji Miyaguchi. Fast Data Encipherment Algorithm FEAL.](https://link.springer.com/chapter/10.1007/3-540-39118-5_24) <br> - [Mitsuru Matsui, Atsuhiro Yamagishi. A New Method for Known Plaintext Attack of FEAL Cipher](https://link.springer.com/chapter/10.1007/3-540-47555-9_7) |
| 4   | - Differential fault analysis of AES | - [Michael Tunstall, Debdeep Mukhopadhyay, Subidh Ali. Differential Fault Analysis of the Advanced Encryption Standard using a Single Fault](https://eprint.iacr.org/2009/575) |
| 5   | - Implement a padding oracle attack on AES-CBC (GRADED) |         |


## Examinable Material
### 0. General Techniques
- Prove that a simple scheme is secure with respect to a security notion.
- If a scheme is not secure with respect to a security notion, show a concrete attack against the security notion
- Given a scheme, analyze its efficiency. For example, the number of keys required for the scheme, number of PRF evaluations needed by the scheme, for an encryption scheme, if the encryption/decryption can be parallelized and so on. 



### 1. Encryption
- Definition of Shannon cipher.
- Definition of perfect security.
- One-time pad and its limitations.
- Prove if a cipher is perfectly secure or not.
- Definition of computational cipher.
- Definition of semantic security (standard and bit-guessing).
- Given that $\mathcal{E}$ is semantically secure, prove that $\mathcal{E}$ (that is a simple variant of $\mathcal{E}$) is (or is not) semantically secure.
- Prove that semantic security is stronger than weaker notions of security.


### 2. Stream Ciphers
- Definition of pseuodo-random generators (PRGs).
- Definition of PRG security.
- Given that $G$ is a secure PRG, prove (or disprove) that $G'$ (that is a simple variant of $G$) is a secure PRG.
- Informally argue why stream cipher is semantically secure.
- Reproduce the parallel and sequential compositions of PRGs. Informally argue about their security.


### 3. Block Ciphers
- Definition of block cipher.
- Security definition of block cipher.
- DES and its variants (e.g., Triple-DES).
- Definition of pseudo-random function (PRF).
- Security definition of PRF.
- PRF switching lemma.
- Deterministic counter mode (constructing PRGs from PRFs).
- The Luby-Rackoff construction (constructing block ciphers from PRFs).
- Tree construction (constructing PRFs from PRGs) and variable length tree construction.


### 4. Chosen Plaintext Attack
- Semantic security against chosen plaintext attack (CPA).
- Generic hybrid construction (PRF + semantically secure cipher).
- Randomized counter mode.
- CBC mode.
- Nonce-based encryption (CTR and CBC).


### 5. Message Integrity
- Definition of a message authentication code
- Constructing MACs from PRFs
- The CBC prefix-free secure PRF (raw CBC-MAC)
- The cascade prefix-free secure PRF
- Attacks on the PRF security and MAC security of the CBC and cascade constructions 
- Encrypted PRF: ECBC and NMAC
- Prefix-free encodings
- CMAC