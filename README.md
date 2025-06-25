Cipher Shield is a secure real-time communication system designed to protect messages using modern cryptographic techniques. The system ensures confidentiality, integrity, authentication, 
and access control in peer-to-peer communication by integrating encryption algorithms, hashing, and digital signatures.

System Workflow
1. Key Exchange
Users generate asymmetric keys (RSA or ECC).
Perform Diffie-Hellman key exchange to derive a shared symmetric key (used for AES).

2. Encrypt & Sign Message
Convert the message to ciphertext using AES (symmetric).
Hash the message with SHA-256.
Create a digital signature of the hash using sender’s private key.

3. Send to Receiver
Send the following:
{ Encrypted Message, Signature, Public Key (if needed) }

4. Receiver Decrypts & Verifies
Decrypt the ciphertext using AES and shared key.
Hash the decrypted message.
Use sender's public key to verify the digital signature.
If hash and signature match → message is valid.

5. Threat Detection
If any mismatch occurs in hash/signature, a threat level is raised.
Messages with altered content are blocked or marked suspicious.


Features
1) End-to-End Encryption using AES, RSA, and ECC
2) Message Integrity & Authentication via Hashing & Digital Signatures
3) Threat Detection Mechanism for message tampering
4) Secure Key Management using Diffie-Hellman Key Exchange
5) AI-driven logic for threat level analysis
6) User-friendly Chat Interface (React.js frontend)
7) Flask-based Backend API for cryptographic processing

Core Cryptographic Modules
i)  AES (Symmetric Encryption) – Fast encryption for session messages.
ii) RSA (Asymmetric Encryption) – Used for secure key exchanges.
iii)ECC (Elliptic Curve Cryptography) – Lightweight, strong public key encryption.
iv) SHA-256 Hashing – Ensures message integrity.
v)  Digital Signature – Used for sender authenticity.
vi) Diffie-Hellman – Key agreement protocol.


Project Structure 
cipher-shield/
│
├── frontend/           # React UI for secure chat
│   ├── components/
│   └── ...
│
├── backend/            # Flask APIs for crypto logic
│   ├── crypto/
│   ├── routes/
│   └── ...
│
├── docs/               # Report and documentation
└── README.md


