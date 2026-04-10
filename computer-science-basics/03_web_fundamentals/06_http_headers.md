# Web Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: HTTP Headers

## 🎯 Objective 
- Understand the role of HTTP headers in client-server communication  
- Identify common request and response headers and their purpose  
- Learn how headers influence how data is transmitted and processed  
- Recognise how headers are used in real-world web applications  
- Understand the security implications of HTTP headers  

## 🧠 Core Concepts Learned 

## HTTP Headers
- HTTP headers are additional pieces of information sent between the client and server in HTTP requests and responses  
- They provide metadata that describe how the request or response should be processed  
- While some headers are optional, many are essential for proper communication between client and server  

## Common Request Headers
- **Host:**
  - Specifies the domain name of the server being requested  
  - Required for servers hosting multiple websites

- **User-Agent:** 
  - Contains information about the client’s browser and operating system  
  - Helps servers to format content to different devices (HTML, JavaScript and CSS)   

- **Content-Length:**
  - Indicates the size of the request body  
  - Helps the server determine when the request data has fully arrived  

- **Accept / Accept-Encoding / Accept-Language:**
  - Define what content types, compression methods, and languages the client supports  
  - Allows the server to optimise the response  

- **Cookie:** 
  - Sends stored data (such as session IDs) back to the server  
  - Used to maintain state between requests  

- **Authorization:**
  - Contains credentials used to authenticate the client  
  - Required for accessing protected resources  

## Common Response Headers
- **Set-Cookie:**
  - Instructs the browser to store data for future requests (like login sessions, user preferences, tracking for shopping carts)

- **Cache-Control:**
  - Defines how and for how long responses can be cached  
  - Improves performance and reduces server load  

- **Content-Type:**
  - Specifies the type of data being returned (HTML, CSS, JavaScript, Images, Videos, PDFs)
  - Allows the browser to process the content correctly  

- **Content-Encoding:**
  - Indicates how the data has been compressed   
  - Helps reduce data transfer size  

## 🛠️ Practical Skills Developed
- Identifying HTTP headers in browser developer tools  
- Analysing request and response headers in web traffic  
- Understanding how headers affect content delivery and behaviour    

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  

## 🔐 Security Relevance
- Headers such as **Authorization** are used to control access to protected resources  
- **Cookies** stored via headers can be targeted in attacks such as session hijacking  
- Misconfigured headers may expose sensitive information (server details)  
- Attackers analyse headers to understand how a web application is structured   

## 📌 Lessons Learned  
⚠️ HTTP headers control how data is sent and received between client and server  
⚠️ Both request and response headers are essential for web communication  
⚠️ Headers play a key role in authentication, performance, and security         