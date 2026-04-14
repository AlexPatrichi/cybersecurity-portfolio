# Data Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe    
Skill Level: Beginner / Foundation   
Focus Area: Data Representation   

## 🎯 Objective
- Understand how data is represented in computer systems using binary  
- Learn how different number systems (binary, decimal, hexadecimal) are used  
- Perform basic conversions between number systems  
- Explore how data representation is used in real-world applications such as color systems  

## 🧠 Core Concepts Learned
## Data Representation
- All data in computers (text, images, audio) is stored and processed as binary (0s and 1s).    
- Different systems are used to represent and interpret this binary data in meaningful ways. 

### Bit and Byte (Fundamental)
- Bit = 1 binary value (0 or 1)    
- Byte (Octet) = 8 bits   
- 1 byte can represent 256 values (0–255)    

💡 Used to measure memory, files, and network data  

### Numeric Representation 
- Decimal (Base-10) → Human system (0–9)
- Binary (Base-2) → Computer system (0,1)
- Hexadecimal (Base-16) → Compact and human-readable representation of binary (0–9, A–F)
    
#### Hexadecimal Reference Table: 
| Decimal | Binary | Hex |
|--------|--------|-----|
| 0 | 0000 | 0 |
| 1 | 0001 | 1 |
| 2 | 0010 | 2 |
| 3 | 0011 | 3 |
| 4 | 0100 | 4 |
| 5 | 0101 | 5 |
| 6 | 0110 | 6 |
| 7 | 0111 | 7 |
| 8 | 1000 | 8 |
| 9 | 1001 | 9 |
| 10 | 1010 | A |
| 11 | 1011 | B |
| 12 | 1100 | C |
| 13 | 1101 | D |
| 14 | 1110 | E |
| 15 | 1111 | F |

### Number Transformations  
**Decimal → Binary**   
Convert 10 (decimal)   

10 ÷ 2 = 5 remainder 0   
5 ÷ 2 = 2 remainder 1   
2 ÷ 2 = 1 remainder 0    
1 ÷ 2 = 0 remainder 1   

Read remainder bottom → top:   
10 (decimal) = 1010 (binary)   

**Binary → Decimal**   
Convert 1010 (binary)   

(1 × 2³) + (0 × 2²) + (1 × 2¹) + (0 × 2⁰)   
= 8 + 0 + 2 + 0   
= 10 (decimal)   

**Binary → Hexadecimal**  
Convert 1010    

Group 4 bits for 1 hex digit    
1   0   1  0     
2³  2²  2¹  2⁰ = 2³ + 2¹ = 8 + 2 = 10 = A (hex)    

**Hexadecimal → Decimal**    
Convert 2F    

Hexadecimal is base-16, which means each position represents a power of 16.  
(2 x 16¹) + (F x 16⁰) = 32 + F(15) = 47 (decimal)   

### Representing Colors    
**Basic RGB (8-Color System)**
- Computers represent colors using RGB system (Red, Green, Blue).
- Uses 3 bits total (1 bit per channel: Red, Green, Blue).
- Each color channel can be: 0 (off) or 1 (on). 
- These states create 8 different colors (2 × 2 × 2 = 8 colors).
- We can use three binary digits to represent RGB states:
    - 111 → White (all on)
    - 100 → Red (only Red on)
    - 000 → Black (all off)

**Modern Color System:**
- Instead of on/off for every RGB, we have now 3 channels with 256 possible values (0–255).
- Total colors:
    256 (Red) × 256 (Green) × 256 (Blue) = 16,777,216 colors
- From 8 to 16 Million Colors (covers more than human needs).

**Hex and Colors**
- Colors are often written in hexadecimal format: #RRGGBB
- Each pair is a hex value (00–FF):
    - 00 = 0 (no intensity)
    - FF = 255 (maximum intensity)

## 🛠️ Practical Skills Developed
- Converting between binary, decimal, and hexadecimal systems  
- Understanding how computers store and process data  
- Interpreting hexadecimal values in real-world contexts (colors)  

## 🧰 Tools Used
- TryHackMe platform
- Solent University Cybersecurity Coursework

## 🔐 Security Relevance
- Binary and hexadecimal are commonly used in cybersecurity (memory addresses, packet data)  
- Understanding data representation helps analyse network traffic and detect anomalies  
- Hexadecimal is widely used in debugging, malware analysis, and forensic investigations  
- Incorrect data interpretation can lead to vulnerabilities or misconfigured systems  

## 📌 Lessons Learned
⚠️ All data in computers (text, images, audio) is ultimately stored as binary (0s and 1s)    
⚠️ Different number systems make binary easier for humans to read and work with    
⚠️ Hexadecimal simplifies long binary values and is widely used in computing    
⚠️ Data representation is essential for understanding how systems store and process information    