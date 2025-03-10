## 1. Encrypted Messaging: The iMessage Protocol
- The iMessage protocol is an old encrypted messaging protocol that does not meet modern security expectations. Still, the iMessage protocol is an interesting subject of studies as the first version of it is totally broken but the security engineers could only patch the design as it needs to be backward compatible. The patched version is better than the first version but it does not achieve 128 bits of security. The iMessage protocol is a prime example for why designing a secure protocol is hard and why cryptograhic agility is important.
- Papers to be presented:
  - https://www.usenix.org/conference/usenixsecurity16/technical-sessions/presentation/garman
  - https://eprint.iacr.org/2020/224


## 2. Encrypted Messaging: The Signal Protocol
- The Signal protocol is the gold standard for E2EE messaging. The protocol provides confidentiality, integrity, authentication, participant consistency, destination validation, forward secrecy, post-compromise security, causality preservation, message unlinkability, message repudiation, participation repudiation, and asynchronicity. It is used in many modern E2EE messaging apps including Signal, WhatsApp, and Google Messages.
You will learn more about the security properties and how the Signal protocol achieves them in the presentation!
- Paper to be presented:
  - https://eprint.iacr.org/2016/1013


## 3. Encrypted Backup of E2EE Messages: The Whatsapp Backup Protocol
- WhatsApp is an end-to-end encrypted (E2EE) messaging service used by billions of people. In late 2021, WhatsApp rolled out a new protocol for backing up chat histories. The E2EE WhatsApp backup protocol (WBP) allows users to recover their chat history from passwords, leaving WhatsApp oblivious of the actual encryption keys. The WBP builds upon the OPAQUE framework for password-based key exchange, which is currently undergoing standardization.
You will learn what the OPAQUE framework is and how WBP is constructed.
- Paper to be presented:
  - https://eprint.iacr.org/2023/843


## 4. E2EE Cloud Storage: MEGA
MEGA is a leading cloud storage platform with more than 250 million users and 1000 Petabytes of stored data. MEGA claims to offer user-controlled, end-to-end security. This is achieved by having all data encryption and decryption operations done on MEGA clients, under the control of keys that are only available to those clients. This is intended to protect MEGA users from attacks by MEGA itself, or by adversaries who have taken control of MEGA’s infrastructure.
It turns out that MEGA is not as secure as one hoped for. It was shown that under the malicious server setting, the confidentiality of user files can be fully compromised by making 512 login attempts. The mumber of login attemps is later reduced to 6, and then to 2!
You will learn how E2EE cloud storage in MEGA works and the pitfalls to avoid when you design your own E2EE cloud storage system.

- Papers to be presented:
  - https://eprint.iacr.org/2022/959
  - https://eprint.iacr.org/2022/914
  - https://eprint.iacr.org/2023/329


## 5. Private Set Intersection
Private set intersection (PSI) is a secure multiparty computation cryptographic technique that allows two parties holding sets to compare encrypted versions of these sets in order to compute the intersection. In this scenario, neither party reveals anything to the counterparty except for the elements in the intersection. PSI has many real-world applications such as private contact discovery, [pasword monitoring](https://support.apple.com/guide/security/password-monitoring-sec78e79fc3b/web), and so on.
There are many known approaches to construct a PSI protocol. In this presentation, you will see a circuit-based PSI based on cuckoo hashing.

- Paper to be presented:
  - https://eprint.iacr.org/2018/120


## 6. Private Information Retrieval
A private information retrieval (PIR) protocol is a protocol that allows a user to retrieve an item from a server in possession of a database without revealing which item is retrieved. One trivial, but very inefficient way to achieve PIR is for the server to send an entire copy of the database to the user. In fact, this is the only protocol that gives the user information-theoretic privacy for their query in a single-server setting (just like one-time pad is required to achieve perfect security).
However, if we relex the privacy requirement to a computational one (just like we relax the security requirement for computational cipher to computational security), we can construct PIRs with much better communication cost. In this presentation, you will see two PIRs with communication overhead logarithmic in the number of the size of the database.

- Papers to be presented:
  - https://eprint.iacr.org/2023/452
  - https://eprint.iacr.org/2023/1072


## 7. Secret Sharing
Threshold secret sharing enables distributing a message to n parties such that no subset of fewer than t parties can learn the message, whereas any subset of at least t parties can recover the message. Threshold secret sharing is a fundamental primitive for secure multiparty computation.
In this presentation, you will see one of the recent papers on secret sharing for large-scale applications.

- Paper to be presented:
  - https://eprint.iacr.org/2024/1045


## 8. Zero-knowledge from Secure Multiparty Computation
A zero-knowledge proof allows a prover to convince a verifier of an assertion without revealing any further information beyond the fact that the assertion is true. Secure multiparty computation allows n mutually suspicious players to jointly compute a function of their local inputs without revealing to any t corrupted players additional information beyond the output of the function.

In this presentation, you will see a new general connection between these two fundamental notions. Specifically, you will see a general construction of a zero-knowledge proof for an NP relation R(x,w) which only makes a black-box use of any secure protocol for a related multi-party functionality f.

- Paper to be presented:
  -https://web.cs.ucla.edu/~rafail/PUBLIC/77.pdf


## 9. Commitment Schemes: Vector Commitments
Vector commitment (VC) schemes are a type of commitment scheme. Informally, VCs allow to commit to an ordered sequence of q values (m1, ..., mq) in such a way that one can later open the commitment at specific positions (e.g., prove that mi is the i-th committed message).
VC has many applications such as verifiable databases with efficient updates, updatable zero-knowledge databases, and universal dynamic accumulators.
In this presentation, you will see two constructions of VCs.

- Paper to be presented:
  - https://eprint.iacr.org/2011/495


## 10. Context Commitment Security
In the lectures, you saw authenticated encryption as the gold standard for an encryption scheme. This turns out to be insufficient in some application. For instance, imagine Alice and Bob use Whatsapp for their communication (where the messages are encrypted with an AE). At some point, Alice wants to report Bob for harmful content. Alice can do this by sending the encrypted message Bob sent to her, the nonce and the key of the message to Meta. However, there is nothing preventing Alice from sending the encrypted message for an innocent message and cleverly crafted nonce and key such that the encrypted message decrypts to some harmful content to Meta. Just to convince yourself (with a simplified example), you can decrypt a message that is encrypted with AES-$CTR with any nonce and key you like and you will get a different message every time!
In this presentation, you will see security notions stronger than AE(AD) and how to construct encryption schemes that satisfy these security notions.

- Paper to be presented:
  - https://www.usenix.org/conference/usenixsecurity22/presentation/albertini
  - https://eprint.iacr.org/2022/268
  - https://eprint.iacr.org/2023/526
  - https://eprint.iacr.org/2024/875