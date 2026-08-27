# Data Fundamentals - TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe  
Skill Level: Beginner / Foundation  
Focus Area: File Formats

## 🎯 Objective
- Understand what file formats are
- How different types of data are stored
- Why different formats are used for images, audio, video, documents, and other data.

## 🧠 Core Concepts Learned
### WHAT IS A FILE FORMAT? 
A file format defines how information is **organized, stored, and interpreted inside a file.**   
A file is essentially a **sequence of bytes**  stored on a storage device. The structure and meaning of those bytes depend on the file format being used.    

Different file formats are designed for different types of data and purposes, such as: 
- `.txt`         → Plain text 
- `.jpg / .png`  → Images  
- `.mp3 / .wav`  → Audio  
- `.mp4 / .mkv`  → Video  
- `.pdf / .docx` → Documents  
- `.zip / .rar`  → Archives   


**Software** needs to understand the rules of a particular file format in order to correctly interpret the data stored within it.

File Format Interpretation
<table align="center">
<tr><td><pre>
               Raw bytes  
                  ↓  
      File format defines the structure  
                  ↓  
      Software interprets the structure  
                  ↓  
Text / Image / Audio / Video / Documents / Archives 
</pre></td></tr></table>  

### FILE EXTENSIONS
A file extension represents the suffix at the end of a filename, usually separated by a period (.). It indicates the **expected file format** and can help the operating system determine which application should open the file.

<table align="center">
<tr><td><pre>
document.pdf  
        └── .pdf = File extension  
</pre></td></tr></table>

**Common examples include:**  
- `notes.txt`       → Plain text
- `photo.jpg`       → JPEG image
- `music.mp3 `      → MP3 audio
- `document.pdf`    → PDF document
- `archive.zip`     → ZIP archive 

A file extension **does not define or guarantee the actual format of the data inside the file.**

<table align="center">
<tr><td><pre>
photo.jpg → rename → photo.txt  
</pre></td></tr></table>

Changing `.jpg` to `.txt` changes only the filename. It does not modify or convert the data stored inside the file.

💡 A file extension is an indicator of the expected file type, not proof of the file's actual contents.  
⚠️ **Security Note**: File extensions can be changed or manipulated to disguise a file. The actual file type can be identified using methods such as file signatures (magic numbers).

### FILE SIGNATURES / MAGIC NUMBERS
A **file signature**, also known as a **magic number**, is a sequence of bytes commonly found at or near the beginning of a file that can help identify its file format.

Unlike a file extension, the signature is part of the **file's actual contents**.

Example: PNG File
<table align="center">
<tr><td><pre>
      image.png
          ↓
89 50 4E 47 0D 0A 1A 0A
          ↓
   PNG File Signature
</pre></td></tr></table>

The bytes `50 4E 47` represent the ASCII characters `PNG`, making the signature particularly easy to recognise.

**Common file signatures include:**
- `JPEG`    → FF D8 FF
- `PNG`    → 89 50 4E 47 0D 0A 1A 0A
- `PDF`     → 25 50 44 46
- `ZIP`     → 50 4B 03 04
- `EXE`     → 4D 5A
- `ELF`     → 7F 45 4C 46

**EXE** → `4D 5A` — Used to identify **Windows executable files**. The bytes `4D 5A` represent MZ in ASCII.  
**ELF** → `7F 45 4C 46` — Used to identify **Linux/Unix executable files**. The bytes `45 4C 46` represent ELF in ASCII.  

💡 File signatures can help detect files with misleading extensions, although a matching signature alone does not guarantee that a file is valid or safe.

### TEXT vs BINARY FILES
Although all files are ultimately made of bytes, they can be interpreted differently depending on how their data is structured.

#### 1. Text Files
A **text file **stores data as characters using a **character encoding**, such as ASCII or UTF-8.

Example: Text stored using UTF-8
<table align="center">
<tr><td><pre>
H    e    l    l    o      ← Text    
48   65   6C   6C   6F     ← Hexadecimal
</pre></td></tr></table>

💡 A **text editor** interprets these bytes as characters, allowing us to see `Hello`.

**Common text-based formats include:**
- `.txt` → Simple text with no special formatting
- `.csv` → Data organised in rows and columns
- `.json` → Organised data commonly used by applications and APIs
- `.xml` → Organised data using tags
- `.html` → Content and structure of a web page
- `.md` → Text with simple formatting, commonly used for documentation
- `.yaml / .yml` → Organised data commonly used for configuration files
- `.log` → Records of events and activity from a system or application

#### 2. Binary Files
A **binary file** contains data structured for software to interpret rather than primarily for humans to read directly.

**Common binary formats include:**
- `.jpg` → Compressed image commonly used for photos
- `.png` → High-quality image that supports transparency
- `.mp3` → Compressed audio, commonly used for music
- `.pdf` → Document designed to keep its layout across devices
- `.exe` → Executable program used by Windows
- `.zip` → Archive used to package and often compress files

Example: Simplified structure of a PNG file
<table align="center">
<tr><td><pre>
PNG
│
├── File signature
├── Image dimensions
├── Colour information
├── Compressed image data
└── Metadata
</pre></td></tr></table>

Software that understands `PNG` format knows how to interpret these bytes and display them as an image.  

If a binary file is opened in a **text editor**, the editor attempts to interpret its bytes as characters. Since most of those bytes were not intended to represent text, the result often appears as unreadable or random characters.  

💡 Both text and binary files are ultimately made of bytes. The difference is how those bytes are structured and interpreted.  


### COMPRESSION 
Compression is the process of reducing the amount of data needed to store a file, resulting in a **smaller file size**.

**Compression is commonly used to:**
- Save storage space
- Reduce download and upload times
- Reduce bandwidth usage
- Make files easier to store and transfer

There are two main types of compression:
1. **Lossless Compression**
Lossless compression reduces file size **without permanently losing any data**. When the file is decompressed, the original data can be restored.

<table align="center">
<tr><td><pre>
Original Data → LOSSLESS COMPRESSION → Smaller File → DECOMPRESSION → Original Data
</pre></td></tr></table>

**Common examples:**
- `PNG` → Lossless image compression
- `FLAC` → Lossless audio compression
- `ZIP` → Lossless file compression

2. **Lossy Compression**
Lossy compression reduces file size by **permanently removing some data**, usually information considered less important or noticeable.

<table align="center">
<tr><td><pre>
Original Data → LOSSY COMPRESSION → Some Data Removed/Lost → Smaller File
</pre></td></tr></table>

**Common examples:**
- `JPEG` → Lossy image compression
- `MP3` → Lossy audio compression

💡 File formats are designed with **specific goals and rules**. Some use lossless compression to preserve data, while others use lossy compression to prioritize smaller file sizes.

#### Compression vs. Archiving
Compression and archiving are related, but they are not the same process.
Compression **reduces the amount of data needed**, while archiving **combines one or more files into a single file**.  
💡 Some formats, such as **ZIP**, can do both.  

#### Compression vs. Conversion
**Compression** reduces the amount of data needed to store a file, while **conversion** changes data from one format to another.

💡 Converting `JPEG → PNG` changes the **file format**; it does not restore data previously lost through JPEG compression.

### MEDIA CONTAINERS AND CODECS
#### 1. Media Containers
A **container** is a file format that can hold different types of media together, such as **video, audio, subtitles, and metadata.**

Example: MP4 Container
<table align="center">
<tr><td><pre>
video.mp4
│
├── 🎬 Video
├── 🎵 Audio
├── 💬 Subtitles
└── 📝 Metadata
</pre></td></tr></table>

**Common container formats include:**
- `.mp4` → Widely used for video and streaming
- `.mkv` → Flexible container that can hold multiple audio and subtitle tracks
- `.webm` → Commonly used for web video
- `.avi` → Older video container format

💡 **The container organises and stores the different media streams together.**

#### 2. Codecs
A **codec** is used to **encode and decode** audio or video data. Codecs often use compression to reduce the amount of data required.

The word codec comes from: `CO`der + `DEC`oder = `CODEC`

**Common codecs include:**
- `H.264` → Common video codec used for streaming and video files
- `H.265 / HEVC` → Video codec designed for better compression
- `AAC` → Common audio codec used with video and streaming
- `MP3` → Widely used audio codec

Example: Inside an MP4 Container
<table align="center">
<tr><td><pre>
video.mp4  
│   
├── 🎬 Video → H.264 codec  
├── 🎵 Audio → AAC codec  
├── 💬 Subtitles  
└── 📝 Metadata  
</pre></td></tr></table>

💡 **The file extension usually identifies the container, but it does not necessarily tell us which codecs are used inside.**

### FILE METADATA
Metadata is additional information stored about a file that helps describe its contents, properties, and origin.

For example, an image may contain more than just the pixels you see:
<table align="center">
<tr><td><pre>
photo.jpg
│
├── 🖼️ Image data
│
└── 📝 Metadata
    ├── Date and time
    ├── Camera/device information
    ├── Image dimensions
    ├── Camera settings
    └── GPS location (if recorded)
</pre></td></tr></table>

💡 Metadata is additional information that describes or provides context about the file.

Metadata isn't limited to photographs:
<table align="center">
<tr><td><pre>
| File type     | Metadata may include                        |
| ------------- | ------------------------------------------- |
| **Documents** | Author, creation date, modification date    |
| **Audio**     | Artist, album, title, genre                 |
| **Video**     | Duration, resolution, codecs, creation date |
| **Images**    | Device, date, dimensions, GPS information   |
</pre></td></tr></table>

🔐 **Privacy and Security**
Metadata can reveal **information that is not visible in the file's main content**, such as the creator, device used, creation date, or GPS location.  

This information may expose sensitive details unintentionally when a file is shared.  
⚠️ Always consider what metadata a file may contain before sharing or publishing it.  

### COMMON FILE FORMATS
#### 🖼️ Images
Image formats store digital visual information. Different formats are designed for different needs such as **quality, file size, transparency, animation, and scalability.**
<table align="center">
<tr><td><pre>
| Format   | Main characteristic             | Common use            |
| -------- | ------------------------------- | --------------------- |
| **JPEG** | Lossy compression, small files  | Photos                |
| **PNG**  | Lossless, supports transparency | Graphics, Screenshots |
| **GIF**  | Supports simple animation       | Short animations      |
| **SVG**  | Vector-based and scalable       | Logos, Icons          |
</pre></td></tr></table>

#### 🎵 Audio
Audio formats store digital sound. They differ mainly in **quality, compression, and file size.**
<table align="center">
<tr><td><pre>
| Format   | Main characteristic                           | Common use               |
| -------- | --------------------------------------------- | ------------------------ |
| **WAV**  | Often uncompressed, High quality, Large files | Recording, Audio editing |
| **MP3**  | Lossy compression, Small files                | Music, General audio     |
| **FLAC** | Lossless compression, High quality            | Music archiving          |  
</pre></td></tr></table>

#### 🎬 Video
Video files can contain **video, audio, subtitles, and metadata**. MP4, MKV, and WebM are commonly used as container formats.
<table align="center">
<tr><td><pre>
| Format   | Main characteristic                         | Common use                 |
| -------- | ------------------------------------------- | -------------------------- |
| **MP4**  | Widely supported, Efficient                 | Streaming, General video   |
| **MKV**  | Supports multiple audio and subtitle tracks | Movies, High-quality video |
| **WebM** | Designed for web-based media                | Online video               |
</pre></td></tr></table>

💡 **MP4, MKV and WebM are containers**. The actual video and audio inside them may use different codecs.

#### 📄 Documents and Data
These formats are used to store **text, structured data, and documents**.
<table align="center">
<tr><td><pre>
| Format   | Main characteristic                | Common use             |
| -------- | ---------------------------------- | ---------------------- |
| **TXT**  | Plain text                         | Notes, Simple text     |
| **CSV**  | Data organised in rows and columns | Spreadsheets, Datasets |
| **JSON** | Structured, Human-readable data    | APIs, Applications     |
| **PDF**  | Preserves document layout          | Reports, Documents     |
| **DOCX** | Editable formatted document        | Word processing        |
</pre></td></tr></table>

#### 📦 Archives
Archive formats are used to **package multiple files together**, often with compression.
<table align="center">
<tr><td><pre>
| Format   | Main characteristic      | Common use                    |
| -------- | ------------------------ | ----------------------------- |
| **ZIP**  | Archive with compression | Sharing and compressing files |
| **RAR**  | Archive with compression | Compressed file collections   |
| **TAR**  | Combines multiple files  | Linux/Unix archives           |
| **GZIP** | Compresses data          | Compression on Linux/Unix     |
</pre></td></tr></table>

💡 **TAR vs GZIP**: TAR combines files into one archive, while GZIP compresses them. A `.tar.gz` file uses both — TAR first, then GZIP.

## 🛠️ Practical Skills Developed
- Identifying common file formats
- Inspecting file extensions
- Identifying files using file signatures
- Viewing files as hexadecimal data
- Inspecting file metadata
- Recognising misleading file extensions

## 🧰 Tools Used
- TryHackMe platform
- Solent University Cybersecurity Coursework

## 🔐 Security Relevance
- File extensions cannot always be trusted.
- Attackers can disguise malicious files using misleading extensions.
- File signatures can help determine a file's actual format.
- Documents and archives can contain malicious content.
- Metadata may unintentionally expose sensitive information.
- Understanding file formats is useful when analysing suspicious files.
 

## 📌 Lessons Learned
⚠️ A file extension does not necessarily represent the file's actual format.  
⚠️ Renaming a file does not convert its contents.  
⚠️ Files can often be identified by inspecting their internal structure.  
⚠️ Metadata can reveal information that is not immediately visible to the user.    