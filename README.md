# SkillChain — Tamper-Proof Certificate Verification

Hackathon Project Submission

Team:
<team name>

Project Repository:
https://github.com/anushaa-m/skillchain

## Problem
Fake certificates and unverifiable achievements make it difficult for employers and institutions to trust digital credentials.

## Solution
SkillChain anchors certificate fingerprints (hashes) onto the Algorand blockchain.  
Instead of storing the certificate itself, the system stores its SHA-256 hash in a blockchain transaction note field.

Any verifier can upload the certificate again → generate the hash → check if the hash exists on blockchain.

If it exists → certificate is authentic.

## Architecture
Frontend: HTML forms  
Backend: Flask API (handles certificate upload + hashing)  
Blockchain Service: Node.js + Algorand SDK  
Blockchain: Algorand TestNet

Flow:
User uploads certificate → Flask generates SHA-256 hash → Node service writes hash to Algorand → transaction ID stored → verification checks blockchain.

## What makes this Web3
The blockchain acts as a decentralized, tamper-proof public registry for credential verification.

No central authority is required to validate certificates.

## Demo Instructions
1. Upload certificate
2. System generates hash
3. Hash stored on Algorand blockchain
4. Re-upload certificate to verify authenticity

First working blockchain anchor transaction:
TXID: GLHJHLWTVTRXGMFIMW7NQS357KH2CET6JWFQPYNBMXW7SGUUDLLA
Network: Algorand TestNet


