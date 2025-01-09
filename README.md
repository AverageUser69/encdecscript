---

# 🛡️ File Encryption & Decryption Script

This is a **Bash script** to perform both **encryption** and **decryption** of files using **symmetric** and **asymmetric** encryption methods.

### Features

- Encrypts and decrypts files with user-friendly prompts.
- Supports **Asymmetric Encryption** (RSA).
- Supports **Symmetric Encryption** (AES, BF, CAST5, RC2, etc.).
- Allows users to create new files and choose from existing ones.
- Can encrypt/decrypt with passwords.

### ⚙️ How to Use

1. **Clone or download** this repository.
2. Open a terminal in the script directory.
3. Run the script with the following command:

```bash
chmod +x encrypt_decrypt.sh
./encrypt_decrypt.sh
```

### 💬 User Input Options

- **Encryption**:
  - Choose between **Asymmetric** and **Symmetric** encryption.
  - For **Symmetric Encryption**, select from a variety of algorithms (e.g., AES, CAST5, RC4).
  - Enter a **password** to encrypt the file.

- **Decryption**:
  - Choose between **Asymmetric** and **Symmetric** decryption.
  - For **Symmetric Decryption**, select the algorithm used and provide the **password**.

### 📝 Code Example for Encryption

1. **Asymmetric Encryption** (RSA):

```bash
openssl genrsa -out privatekey 2048
openssl rsa -in privatekey -out publickey -pubout
openssl rsautl -encrypt -inkey publickey -pubin -in <input_file> -out <output_file>
```

2. **Symmetric Encryption** (AES):

```bash
openssl enc -aes-128-cbc -md sha512 -pbkdf2 -iter 10000 -salt -in <input_file> -out <output_file> -k <password>
```

### 🔐 Supported Encryption Algorithms

- **AES (128, 192, 256)**: `aes-128-cbc`, `aes-128-ecb`, `aes-192-cbc`, etc.
- **Blowfish**: `bf-cbc`, `bf-ecb`, etc.
- **CAST5**: `cast5-cbc`, `cast5-ecb`, etc.
- **RC2**: `rc2-cbc`, `rc2-ecb`, etc.
- **RC4**, **Seed** encryption algorithms, and more.

### 🛠️ Troubleshooting

If you encounter any errors during encryption or decryption, ensure:

- You have OpenSSL installed and properly configured.
- The input file paths and output file names are valid.
- If decryption fails, check that the correct password is entered.

### 💡 Helpful Tips

- **For file creation**: If you don't have an existing file, you can create a new one by choosing the option to input file content manually.
- **For decryption**: Make sure you know which algorithm was used to encrypt the file.

### 🏁 Exit the Script

To exit the script at any time, simply type `0` when prompted.

---
