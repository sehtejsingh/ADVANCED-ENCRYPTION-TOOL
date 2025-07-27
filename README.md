# ADVANCED-ENCRYPTION-TOOL

# PENETRATION-TESTING-TOOLKIT

*Company*: CODTECH IT SOLUTION

*Name*: SEHTEJ SINGH

*Itern ID*: : CT04DH922

*Domain*: CYBERSECURITY AND ETHICAL HACKING

*Duration*: 4 Week

*Mentor*: Neela Santosh

Task Description This repository contains the source code for the "Advanced Encryption Tool," a command-line application developed as the fourth and final task for the CodTech IT Solutions internship program. The primary objective of this project was to design and implement a robust, secure, and user-friendly tool capable of encrypting and decrypting files using the AES-256 algorithm, a globally recognized standard for data protection.

The application is built entirely in Python, a versatile and powerful language well-suited for both rapid development and complex operations. The core cryptographic functionalities are handled by the cryptography library, which is a leading, high-level cryptographic library in the Python ecosystem. Relying on this library ensures that the underlying cryptographic primitives are implemented correctly and securely, mitigating the risks associated with building custom cryptographic functions from scratch.

Core Algorithm: AES-256 The heart of this tool is the Advanced Encryption Standard (AES) with a 256-bit key. AES is a symmetric-key algorithm, meaning the same key is used for both the encryption and decryption processes. The 256-bit key length is currently considered the gold standard for securing sensitive information, offering an exceptionally high level of security against brute-force attacks.

To enhance security, the encryption is implemented using Cipher Block Chaining (CBC) mode. In CBC mode, each block of plaintext is XORed with the previous ciphertext block before being encrypted. This dependency ensures that even if two plaintext blocks are identical, their corresponding ciphertext blocks will be different. To start this process, an Initialization Vector (IV) is used for the first block. A new, cryptographically random 16-byte IV is generated for every single encryption operation, which is crucial for preventing pattern analysis and ensuring that encrypting the same file multiple times with the same key results in a completely different ciphertext each time. This IV is not secret and is prepended to the ciphertext, as it is required for decryption.

Furthermore, since AES is a block cipher that operates on fixed-size blocks of data (16 bytes), the tool implements PKCS7 padding. This standard padding scheme ensures that the final block of plaintext is always filled to the required size before encryption, allowing the tool to handle files of any size without data loss or corruption.

Application Architecture and Features The Python script is structured logically into two main parts: the core cryptographic functions and the user-facing main application logic.

Key Management: The tool provides a function to generate a new, secure 256-bit key and save it to a file. It also includes a function to load an existing key, which is necessary for both encryption and decryption.

File Encryption/Decryption: Separate, dedicated functions handle the file I/O and cryptographic operations for encrypting and decrypting files, keeping the logic clean and modular.

User-Friendly Command-Line Interface (CLI): The main function creates an interactive and intuitive menu-driven interface. It guides the user through the available options: generating a key, encrypting a file, or decrypting a file. This design choice makes the powerful cryptographic functions accessible even to users who may not be familiar with the underlying technology.

Error Handling: The application includes robust error handling to gracefully manage common issues such as incorrect file paths (FileNotFoundError), invalid user input, or potential decryption failures (e.g., using the wrong key), providing clear feedback to the user.

This project was a significant learning experience, providing deep insights into the practical application of modern cryptography. It required a thorough understanding of symmetric-key algorithms, block cipher modes, padding schemes, and the critical importance of secure key management. The development process involved researching best practices, understanding the cryptography library's API, and designing a user interface that is both functional and easy to navigate. The final result is a powerful and reliable tool that successfully meets all the requirements of the internship task.
