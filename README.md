
#  Bash Script for File Encryption and Decryption

SecureFileEncrypt is a Bash script designed to provide a simple and secure way to encrypt and decrypt files. It supports both asymmetric (RSA) and symmetric encryption algorithms, allowing users to protect their data with a password or key pair. Whether for personal or professional use, this tool enables seamless file encryption and decryption from the command line.


## Features
- Supports **Asymmetric Encryption** (RSA) and **Symmetric Encryption** (AES, Blowfish, CAST5, etc.)
- Allows **password-based encryption** and decryption.
- Enables creation of **new files** for encryption or choosing **existing files**.
- **User-friendly prompts** for selecting encryption type, algorithm, and file paths.
- **Secure file protection** with multiple encryption algorithms to choose from.
- Provides an easy way to **decrypt** files with the correct password or algorithm. 
- Option to **exit the script** at any time with a simple command.




## Troubleshooting
If you encounter any errors during encryption or decryption, ensure:

You have OpenSSL installed and properly configured.
The input file paths and output file names are valid.
If decryption fails, make sure the correct password is entered.

## Helpful Tips
For file creation: If you don't have an existing file, you can create a new one by choosing the option to manually input file content.
For decryption: Make sure you know which algorithm was used to encrypt the file.

