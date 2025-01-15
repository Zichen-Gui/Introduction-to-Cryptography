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
| 6       | - Block Cipher <br> - Encryption with block cipher directly <br> - Pseudorandom functions <br> - PRF Switching lemma <br> - Constructing block cipher from PRFs (the Luby-Rackoff construction) | - Boneh&Shoup 4.1, 4.4, 4.5 |


## Labs
| Lab | Topic(s)                                       | Remarks |
|-----|------------------------------------------------|---------|
| 1   | - Implement One-Time Pad <br> - Attack Two-Time Pad |         |
| 2   | - Attack `Math.random()` in Java 8 <br> - Implement the Content Scrambling System (CSS). <br> - Attack CSS |         |


## Examinable Material
### 1. Encryption
- Definition of Shannon Cipher.
- Definition of perfect security.
- One-time pad and its limitations.
- Prove if a cipher is perfectly secure or not.
- Definition of Computational Cipher.
- Definition of semantic security (standard and bit-guessing).
- Given that $\mathcal{E}$ is semantically secure, prove that $\mathcal{E}$ (that is a simple variant of $\mathcal{E}$) is (or is not) semantically secure.
- Prove that semantic security is stronger than weaker notions of security.


### 2. Stream ciphers
- Definition of Pseuodo-random generators (PRGs).
- Definition of PRG security.
- Given that $G$ is a secure PRG, prove (or disprove) that $G'$ (that is a simple variant of $G$) is a secure PRG.
- Informally argue why stream cipher is semantically secure.
- Reproduce the parallel and sequential compositions of PRGs. Informally argue about their security.
