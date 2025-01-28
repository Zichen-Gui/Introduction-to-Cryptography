# CSCI 4900/6900 Introduction to Cryptography
Welcome to the course repository of CSCI 4900/6900 Introduction to Cryptography! You can find an overview of the course below (updated weekly). The programming exercises of the course are in the `Labs` folder.


## Lectures
| Lecture | Topic(s)                                                                                                                                             | Remarks             |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| 1       | - History of cryptography <br> - Aim of modern cryptography <br> - Shannon Cipher and perfect security <br> - Computational ciphers and semantic security (informal) | - Boneh&Shoup 2.1     |
| 2       | - Semantic security (formal) <br> - Why should everyone care about cryptography? | - Boneh&Shoup 2.2 <br> - [Sudheendra Raghav Neela. The Workings of WhatsApp’s Backups (and Why You Should Enable End-to-End Encrypted Backups)](https://snee.la/posts/the-workings-of-whatsapps-end-to-end-encrypted-backups/) <br> - [Daniel J. Solove. 'I've Got Nothing to Hide' and Other Misunderstandings of Privacy](https://scholarship.law.gwu.edu/faculty_publications/158/)   |
| 3       | - Pseudorandom generators (PRGs) <br> - Limitation of stream cipher (built from PRGs) <br> - Parallel composition of PRGs | - Boneh&Shoup 3.1-3.4 |
| 4       | - Sequential composition of PRGs (the Blum-Micali construction) <br> - The subset sum generator <br> - The Salsa and Chacha PRGs | - Boneh&Shoup 3.4, 3.6, 3.7.2 |
| 5       | - Linear congruential generator <br> - The Content Scrambling System (CSS) <br> - Pseudorandom Number Generator (PRNG) <br> - Generating random bits in practice | - Boneh&Shoup 3.7.1, 3.8, 3.10 <br> -  [Massimiliano Taverna and Kenneth G. Paterson. Snapping Snap Sync: Practical Attacks on Go Ethereum Synchronising Nodes](https://www.usenix.org/conference/usenixsecurity23/presentation/taverna)|
| 6       | - Block Cipher <br> - DES/Double-DES/Triple-DES <br> - AES (do not implement your own primitive!) <br> - Pseudorandom function | - Boneh&Shoup 4.1, 4.2, 4.4 <br> - [Ping Wang, Shishir Nagaraja, Aurelien Bourquard, Haichang Gao, Jeff Yan. SoK: Acoustic Side Channels](https://arxiv.org/abs/2308.03806) <br> - [Computerphile (Presented by Mike Pound, original paper by Nassi et al.). Power LED Attack](https://www.youtube.com/watch?v=vXe8pe18MNk) |
| 7       | - PRF Switching Lemma <br> - Constructing PRGs from PRFs <br> - Deterministic counter mode <br> - Constructing block ciphers from PRFs <br> - Constructing PRFs from PRGs | - Boneh&Shoup 4.4, 4.5, 4.6 <br>  |
| 8       | - Semantic security against chosen plaintext attack (CPA) <br> - ECB and deterministic counter modes are not secure against CPA <br> - Generic hybrid construction <br> - Randomized counter mode <br> - Randomized CBC mode | - Boneh&Shoup 5.1-5.4 <br>  |

## Labs
| Lab | Topic(s)                                       | Remarks |
|-----|------------------------------------------------|---------|
| 1   | - Implement One-Time Pad <br> - Attack Two-Time Pad |         |
| 2   | - Attack `Math.random()` in Java 8 <br> - Implement the Content Scrambling System (CSS). <br> - Attack CSS |         |
| 3   | - Implement FEAL <br> - Attack FEAL | -  [Akihiro Shimizu, Shoji Miyaguchi. Fast Data Encipherment Algorithm FEAL.](https://link.springer.com/chapter/10.1007/3-540-39118-5_24) <br> - [Mitsuru Matsui, Atsuhiro Yamagishi. A New Method for Known Plaintext Attack of FEAL Cipher](https://link.springer.com/chapter/10.1007/3-540-47555-9_7) |
| 4   | - Differential Fault Analysis of AES | - [Michael Tunstall, Debdeep Mukhopadhyay, Subidh Ali. Differential Fault Analysis of the Advanced Encryption Standard using a Single Fault](https://eprint.iacr.org/2009/575) |


## Examinable Material
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
