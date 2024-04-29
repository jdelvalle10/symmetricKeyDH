# symmetricKeyDH
Encryption example using the DH Exchange
# Diffie-Hellman Key Exchange Protocol Implementation

## Overview
This script implements a simple version of the Diffie-Hellman key exchange protocol. The Diffie-Hellman key exchange protocol allows two parties to establish a shared secret key over an insecure channel without prior communication. This shared secret key can then be used for secure communication using symmetric encryption.

## Usage
To use this script, follow these steps:

1. Run the script in a Python environment.
2. The script will generate two random prime numbers, `p` and `g`, and compute their primitive roots.
3. Alice and Bob will each generate their private keys (`a` and `b`, respectively) and compute their public keys (`A` and `B`, respectively) using the generated prime numbers and primitive roots.
4. Alice and Bob will calculate the shared secret key (`shared_secret_key_A` and `shared_secret_key_B`, respectively) using their private keys and the other party's public key.
5. The script will then check if the shared secret keys match.
6. Additionally, the script provides functions to encrypt and decrypt messages using the shared secret key.

## Components
- **isPrime(number)**: Checks if a given number is prime.
- **generatePrime()**: Generates a random prime number greater than 10 and less than 100,000.
- **primitiveRoot(prime)**: Calculates a primitive root of a given prime number.
- **printTable(a, b, A, B, Sa, Sb)**: Prints a table with Alice's private key (`a`), Bob's private key (`b`), Alice's public key (`A`), Bob's public key (`B`), and the shared secret key for Alice (`Sa`) and Bob (`Sb`).
- **encrypt(message, key)**: Encrypts a message using the hash of the common secret as the key.
- **decrypt(encrypted_message, key)**: Decrypts a message using the hash of the common secret as the key.

## File Requirements
- The script assumes the presence of a file named `message.txt`, containing the message to be encrypted.

