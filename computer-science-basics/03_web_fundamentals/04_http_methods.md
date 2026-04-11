# Web Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: HTTP Methods

## 🎯 Objective
- Understand how HTTP methods define actions performed on web resources  
- Identify the most commonly used HTTP methods and their purpose  
- Learn how different methods affect server-side data  
- Recognise how HTTP methods are used in real-world web applications  
- Understand the security implications of different request methods  

## 🧠 Core Concepts Learned 
## HTTP Methods
- HTTP methods define the type of action a client wants to perform on a resource hosted on a web server 

### Common Methods
1. **GET Request** 
- Used to get information from a web server 
- Will not modify server-side data (read-only)
- Sometimes visible in the URL 
- Example: Loading a webpage

2. **POST Request**
- Used to send data to the server and potentially creating new records
- This request modifies server data
- Example: Submitting a login or registration form  

3. **PUT Request**
- Common for submitting data to a web server to update or replace information
- Typically replaces the entire resource 
- Example: Updating a full user profile  

4. **DELETE Request**
- Used to remove a resource from the server  
- Example: Deleting a user account 

## 🧪 TryHackMe Lab Example (HTTP Request Emulator)
- Used an HTTP request emulator to build and test demo web requests  

### Tasks Performed:
- Created HTTP requests using the emulator interface  
- Observed how different request methods interact with a web server  
- Analysed the request and response structure  
- Applied knowledge of HTTP learned from previous tasks to complete practical challenges  

### Key Observations: 
- Requests can include methods, headers, and other data depending on their purpose  
- Servers respond with status codes and content based on the request received  
- Understanding the structure of requests helps explain how websites and APIs communicate  

💡 HTTP emulators are useful for visualising how web requests are built and processed  

## 🛠️ Practical Skills Developed
- Identifying HTTP methods in web traffic  
- Understanding how different requests interact with server resources  
- Analysing how data is sent and received between client and server  

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  

## 🔐 Security Relevance
- **GET requests** can expose sensitive data if parameters are included in the URL  
- **POST requests** are safer for transmitting sensitive data, but still require HTTPS encryption  
- Improper use of HTTP methods can lead to vulnerabilities such as **unauthorised data modification**   
- Attackers may exploit misconfigured endpoints using methods like DELETE or PUT  

## 📌 Lessons Learned  
⚠️ Different HTTP methods have different impacts on server data   
⚠️ Not all requests are safe — some can modify or delete data   
⚠️ Understanding HTTP methods is essential for analysing web applications     