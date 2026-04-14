# Data Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Data Encoding

## 🎯 Objective
- Understand how data is represented and encoded in computer systems  
- Learn how text is converted into binary for storage and transmission  
- Identify the limitations of early encoding systems and how modern standards solve them  

## 🧠 Core Concepts Learned
## Data Encoding   
-  While data representation defines how data exists in binary, **encoding defines how that data is interpreted as meaningful text and symbols**.

<p align="center">
<strong>Evolution of Text Encoding</strong><br><br> 
ASCII (1963)<br>
↓<br>
Extended ASCII (8-bit)<br>
↓<br>
ISO-8859 (Regional Standards)<br>
↓<br>
Unicode (Universal Standard)<br>
↓<br>
UTF Encodings (UTF-8, UTF-16, UTF-32)
</p>  

### 🔤 ASCII (American Standard Code for Information Interchange)
- Is an early character encoding (1963) that uses 7 bits to represent numbers 0-127 for English only letters, digits, punctuation, and some control characters. 
- Acts as a small dictionary between text and numeric codes, allowing computer systems to store text in a standardised way.

**ASCII values**  
"HELLO" is actually: 72 69 76 76 79   

**Each ASCII value is stored in binary:**  
H = 72 → 01001000   
E = 69 → 01000101  
L = 76 → 01001100  
L = 76 → 01001100  
O = 79 → 01001111  

#### ASCII Limitations & European Languages
- Using 8 bits allows up to 256 characters, but this was still not enough to support all European languages.
- Extending ASCII solved some problems, but created compatibility issues between different regions.

<div align="center">

<strong>ISO-8859 Standards</strong><br><br>

<table>
  <tr>
    <td width="300px" valign="top">

**ISO-8859-1 (Latin-1)**  
- Western Europe  
- Examples: ñ, ü, é, ç  

    </td>
    <td width="300px" valign="top">

**ISO-8859-2 (Latin-2)**  
- Central/Eastern Europe  
- Examples: ł, č, ș  

    </td>
  </tr>
</table>

</div>

### 🌐 Unicode Standard
- A universal standard for representing all characters from all languages.
- Includes letters from all languages, symbols and emojis.
- Supports over 100,000 characters, including letters, symbols, and emojis.

#### UTF Encoding Formats  
**UTF-8** 
- Most common encoding on the modern web and a default in most systems.
- Backward compatibility with ASCII.
- Uses 1 to 4 bytes per character. 
- Dynamically decides on the number of bytes based on the character complexity: 
    - ASCII characters use exactly 1 byte (same as ASCII)
    - Non-ASCII characters (complex symbols) use 2 bytes
    - Emoji require 4 bytes

**UTF-16**
- Less efficient for simple text than UTF-8 
- Uses either 2 or 4 bytes per character:
    - Most characters → 2 bytes
    - Rare characters or Emojis → 4 bytes (two 16-bit units totaling 4 bytes)

**UTF-32**
- Is the simplest but also the most wasteful
- Rarely used in practice
- Every Unicode code point uses exactly 4 bytes (fixed length) 

## 🛠️ Practical Skills Developed
- Converting text to ASCII and binary representation  
- Understanding differences between encoding standards  
- Recognising encoding formats used in real-world systems

## 🧰 Tools Used
- TryHackMe platform
- Solent University Cybersecurity Coursework

## 🔐 Security Relevance
- Encoding is used to safely transmit and store data across systems  
- Misunderstanding encoding can lead to vulnerabilities such as injection attacks   
- Understanding encoding is essential for analysing network traffic and detecting malicious payloads 

## 📌 Lessons Learned
⚠️ Text is not stored as characters but as numeric values in binary   
⚠️ Early encoding systems like ASCII were limited and region-specific   
⚠️ Unicode solved compatibility issues by creating a universal standard   
⚠️ UTF-8 is widely used because it balances efficiency and compatibility   