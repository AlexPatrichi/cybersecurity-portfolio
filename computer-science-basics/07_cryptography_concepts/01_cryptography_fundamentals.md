# Security Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Cryptography Fundamentals  

## 🎯 Objective
- Understand the purpose of cryptography in securing data  
- Learn the difference between encryption, hashing, and encoding  
- Identify key concepts such as plaintext, ciphertext, and keys  

## 🧠 Core Concepts Learned
## Cryptography Fundamentals
- Cryptography is the practice of securing information using mathematical techniques  
- It protects data from unauthorised access during storage and transmission  

💡 Data often travels through multiple systems — cryptography ensures it cannot be read or modified by attackers  

### Why Cryptography Matters
- Data can be intercepted while travelling across networks  
- Without protection, attackers could read, modify, or block sensitive information  

💡 Cryptography ensures:
- Confidentiality (data remains private)  
- Integrity (data is not altered)  

---

### Key Concepts
- **Plaintext** → Readable data ("HELLO")  
- **Ciphertext** → Scrambled data ("KHOOR")  
- **Key** → Secret value used to encrypt/decrypt data  
- **Algorithm** → The method used to transform data  

💡 Everyone can know the algorithm. Security comes from keeping the key secret

### Encryption Process
- Plaintext + Algorithm + Key → Ciphertext  

### Decryption Process
- Ciphertext + Algorithm + Key → Plaintext  

### 🧪 Plaintext versus Ciphertext Tryhackme Example: 
- Alice wants to send: **HELLO**   
💡 That's the plaintext—the readable message

- Alice uses an algorithm and a secret key to scramble it: **KHOOR**  
💡 That's the ciphertext. To anyone without the key, KHOOR is meaningless

- Bob receives KHOOR, uses the same key and algorithm, and unscrambles it back to HELLO

---

### Encryption vs Hashing vs Encoding
- These techniques transform data for different purposes

#### Encryption
- Transforms plaintext into unreadable ciphertext, requiring a specific secret key to decrypt and recover the original data
  - Reversible process  
  - The main goal of encryption is to ensure data confidentiality 
  - Requires a key  

- Used for securing sensitive data at rest or during transmission (VPNs, HTTPS)

**Example: AES Algorithm, RSA Algorithm, Diffie Hellman**

#### Hashing
- Hashing is a technique where the data is converted to hash using different algorithms
- Hashing is simply used for checking the integrity of the data
  - Does not use a secret key
  - One-way process (cannot be reversed to its original form)  
  - Used for integrity and password storage  

**Example: MD5, SHA256, SHA - 3** 

#### Encoding
- Is a technique to transform data from one format to another, so that it can be understood and consumed by different systems
  - Information representation
  - Has no security purpose
  - Used to convert data into a different format 
  - Encoding is a reversible process

**Example: BASE64, UNICODE, ASCII, URL Encoding** 

💡 Important: Encoding ≠ Encryption  

---

### 🧪 Simple Example: Caesar Cipher
- Technique used over 2000 years ago to send military messages  
💡 Even back then, people understood the value of keeping communications secret
- A basic encryption method that shifts letters by a fixed number  

#### How It Works
- The Caesar cipher shifts each letter in your message by a fixed number of positions in the alphabet 
- That fixed number is your **key**

Example Key of 3:   
Encrypt HELLO → KHOOR      
    H → K  
    E → H  
    L → O  
    L → O  
    O → R  

To decrypt KHOOR, shifts each letter backwards by 3:  
    K → H  
    H → E  
    O → L  
    O → L  
    R → O  

💡 The algorithm is public, but security comes from keeping the key secret
💡 Used for learning only — not secure in real-world systems  
💡 It's simple to understand and shows you how keys and algorithms work together

---

### 🧪 Practical Example: Password Hashing
When a system says: "Your password is stored as a hash"  

It means:  
- The system does NOT store your actual password  
- It stores a hashed version instead  

Login Process  
1. You enter your password  
2. The system hashes it  
3. The system compares it with the stored hash  

👉 If they match → access is granted  

💡 The original password is never stored or revealed  
💡 This makes it harder for attackers to recover passwords if a database is leaked  

## 🛠️ Practical Skills Developed
- Understanding how encryption transforms data  
- Distinguishing between encryption, hashing, and encoding  
- Identifying basic cryptographic concepts in real-world systems  

## 🧰 Tools Used
- TryHackMe platform  
- Solent University Cybersecurity Coursework  

## 🔐 Security Relevance
- Encryption protects sensitive data during transmission (HTTPS)  
- Hashing ensures data integrity and secure password storage  
- Weak cryptography can lead to data breaches and system compromise  

💡 Cryptography directly supports the CIA Triad:
- Encryption → Confidentiality  
- Hashing → Integrity  

## 📌 Lessons Learned
⚠️ Cryptography protects data from unauthorised access  
⚠️ Encryption is reversible, hashing is not  
⚠️ Encoding is not a security mechanism  
⚠️ Strong cryptography is essential for secure systems  