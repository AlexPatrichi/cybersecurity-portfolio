# Software Basics – TryHackMe and Solent University

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: Cybersecurity Fundamentals  

## Objective  
- Understanding that all data (numbers, text, images, network traffic) is stored as **binary**
- Recognise that systems like decimal and hexadecimal are human-friendly representations
- Understand ASCII and its limitations
- Understand Unicode and UTF encodings (UTF-8, UTF-16, UTF-32)
- Understand how text and emojis are encoded

## Core Concepts Learned
### Data Representation 
### 🎨 1. Representing Colors    
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

**Bit and Byte (Fundamental)** 
- Bit = 1 binary value (0 or 1)    
- Byte (Octet) = 8 bits

Used to measure memory, files, and network data.

### 🔢 2. Numeric Representation 
- Decimal (Base-10) → Human system (0–9)
- Binary (Base-2) → Computer system (0,1)
- Hexadecimal (Base-16) → Short form of binary (0–9, A–F)
    
Hexadecimal Reference Table: 
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

### 🔄 3. Number Transformations  
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



### Python: Simple Demo 
### Java Script: Simple Demo
### Database SQL Basics


## Actions Taken
- Learned how data is represented in binary, decimal, and hexadecimal
- Practiced number conversions
- Explored how colors and text are encoded
- Understood encoding evolution (ASCII → Unicode → UTF)

## Tools Used
- TryHackMe platform
- Manual calculations and conversions
- Phyton, Java Script and SQL lab virtual machines 

## Security Relevance
### Data Representation 
- Logs, memory, and network data are often shown in **hexadecimal**
- Understanding number conversions helps with:
  - Reading packet data in tools like **Wireshark**
  - Analysing malware behaviour
  - Decoding payloads and raw data

### Data Encoding
- Text encoding is still widely used in cybersecurity analysis
- It appears in:
  - Logs
  - Network traffic
  - File analysis

- Understanding encoding helps with:
  - Encoding and decoding data correctly
  - Inspecting text-based payloads
  - Identifying unusual or manipulated character data
