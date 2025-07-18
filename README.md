# Secure-QR-using-hasing
Secure QR Code Generator with AES & HMAC
This project implements a secure QR code generation and decryption system using AES-GCM encryption and HMAC-SHA256 for tamper detection. It manually handles key generation, base64 encoding/decoding, and embeds the encrypted data in a QR code. The project includes QR scanning support and data integrity verification.

**Features**
 AES-256 GCM Encryption with 96-bit nonce

 HMAC-SHA256 for integrity verification

 Manual base64 encoding/decoding

 QR Code generation and scanning

Detects tampering using cryptographic hash comparison

**How It Works**


**Generate Keys**
AES and HMAC keys are generated manually using a random byte generator.

**Encrypt Data**
A message is encrypted using AES-GCM. An HMAC-SHA256 hash is generated from the ciphertext and nonce.

**Create QR Code**
The encrypted payload (ciphertext, nonce, auth tag, and HMAC) is embedded into a QR code.

**Scan QR Code**
The QR code is scanned and the encrypted data is extracted.

**Decrypt and Verify**
The data is decrypted and verified using the original keys. If the HMAC doesn't match, the data is considered tampered.
