# Network Security

Information Security:

- confidentiality (restrict access)
- integrity (no modification)
- availability (available when needed)

## Basics

### Confidentiality

Send a message and keep it secret from all parties but the recipient.

Achieved via cryptography - plaintext into ciphertext. You need the decryption
key to decrypt ciphertext.

##### Symmetric Encryption

Shared key used for both encryption and decryption

```
E
4 5
0100 0101
XOR 1101 0111 (key)
= 1001 0010

can be decrypted XORing with same key
```

Common used example: AES

##### Asymmetric Encryption

Decryption machine generates public and private key.
Anyone can encrypt with public key but only you can decrypt with private key.

Example: RSA

##### Session Key

Use asymmetric encryption to transport short lived symmetric encryption keys

### Integrity

Hash function - calculate a fixed length digest from a variable length message
Should be computationally infeasible to find another message that would result
in the same message digest.

HMAC (hash keyed message authentication code)

sender and reciever share a secret key - `H(key | H(key | message))`

Digital signatures: use asymmetric keys to enable checking the message has not
changed and that it came from the correct sender. Alice uses private key to
sign, Bob uses Alice's public key to verify.

Digital certificates: bind a public key and identity. A certificate authority
verifies identity and signs the certificate with their private key. The CA's
public key is trusted (pre-installed in a browser)
