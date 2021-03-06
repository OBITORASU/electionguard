# ElectionGuard Glossary

## Overview

ElectionGuard, end-to-end verifiability, and elections themselves use a variety of terms in the conductance of an election, as well as the encryption, tally, and publishing thereof. Many of these terms have variants used in different locales. Given the potential ambiguity of terminology, we present this Glossary. It states the precise meaning and usage of the terms used by the ElectionGuard SDK and related specifications and tools.

Whenever possible, we used terms and meanings consistent the [NIST Elections Guide](https://pages.nist.gov/ElectionEventLogging/index.html).

## Terms

### Accepted Ballot 
A ballot that is accepted for inclusion in election results and is either: cast or spoiled.

### Auxiliary Key Pair
Pair of keys (public & secret) used to encrypt/decrypt information sent between guardians

### Available Guardian
A guardian that has announced as present for the decryption phase

### Ballot Box
A collection of ballots that have been either cast or spoiled.

### Cast Ballot
A ballot which a voter has accepted as valid to be included in the official election tally.

### Ciphertext Ballot
An encrypted representation of a voter's filled-in ballot.

### Ciphertext Election Context
The cryptographic context of an election that is configured during the Key Ceremony

### Compensated Decryption Share
A partial decryption share value computed by an available guardian to compensate for a missing guardian so that the missing guardian's share can be generated and the election results can be successfully decrypted.

### Description Hash
A hash representation of the original election description.

### Decryption Mediator
A component or actor responsible for composing each guardian's partial decryptions or compensated decryptions into the plaintext tally

### Decryption Share
A guardian's partial share of a decryption

### Election Description
The election metadata that describes the structure and type of the election, including geopolitical units, contests, candidates, and ballot styles, etc.

### Encryption Device
The device that is doing the encryption

### Election Key Pair
Pair of keys (public & secret) used to encrypt/decrypt election

### Election Manifest
The election metadata in json format that is parsed into an Election Description

### Election Partial Key Backup
A point on a secret polynomial and commitments to verify this point for a designated guardian.

### Election Polynomial
The election polynomial is the mathematical expression that each Guardian defines to solve for his or her private key. A different point associated with the polynomial is shared with each of the other guardians so that the guardians can come together to derive the polynomial function and solve for the private key.

### Encrypted Tally
The homomorphically-combined and encrypted representation of all selections made for each option on every contest in the election.

### Guardian
A guardian of the election who holds the ability to partially decrypt the election results

### Homomorphic Tally
An encrypted representation of every selection on every ballot that was cast.  

### Internal Election Description
The subset of the election description required by ElectionGuard to validate ballots are correctly associated with an election.  This component mutates the state of the Election Description.

### Joint Key 
Combined public key from election public keys of each guardian

### Key Ceremony 
The process conducted at the beginning of the election to create the joint encryption context for encrypting ballots during the election.

### Key Ceremony Mediator
A mediator to mediate communication (if needed) of information such as keys between the guardians

### Missing Guardian
A guardian who was configured during the Key Ceremony but who is not present for the decryption of the election results.

### Nonce
A random number used to derive encryptions

### Plaintext Ballot 
The plaintext representation of a voter's selections

### Quorum
The minimum count (_threshold_) of guardians that must be present in order to successfully decrypt the election results.

### Spoiled Ballot
A ballot which a voter did not accept as valid and is not included in the tally.

### Tracking Code
A unique hash value generated by an Encryption Device to anonymously identify a ballot

### Unknown Ballot
A ballot which may not yet be determined as cast or spoiled, or that may have been spoiled but is otherwise not published in the election results.
