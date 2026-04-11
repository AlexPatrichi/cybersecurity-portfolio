# Web Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: HTTP Status Codes

## 🎯 Objective 
- Understand what HTTP status codes represent in client-server communication  
- Learn the different categories of status codes and their meanings  
- Identify common status codes and their real-world usage  
- Recognise how status codes are used in troubleshooting and web analysis  
- Understand the security implications of different server responses  

## 🧠 Core Concepts Learned 
## HTTP Status Codes
- Are **3-digit response codes** that server sends back to the client (browser) after a request is made 

### Main Groups: 
- **100 - 199 Informational Responses**
    - Indicate that the request has been received and the process is continuing
    - Rarely seen in everyday web browsing  

- **200–299 Success**
    - Tells the client that their request was successful received, understood, and processed  

- **300–399 Redirection**
    - Indicate that further action is needed to complete the request  
    - Usually involves redirecting the client to another resource (Different Webpage or Website)  

- **400–499 Client Errors**
    - Tells the client that was an error with their request (incorrect syntax or unauthorised access)

- **500–599 Server Errors**
    - Reserved for errors happening on the server-side
    - Usually indicating problems with the servers handling the request

### Most Common Status Codes
- **200 OK**
  - Request successful, resource returned  

- **201 Created**
  - Resource successfully created 
  - Often after POST request (new user or blog post) 

- **301 Moved Permanently**
  - Resource has been permanently moved to a new URL  

- **302 Found**  
  - Temporary redirection to another resource  
  - Unlike **301**, the original URL may be used again in the future  

- **400 Bad Request**
  - Invalid request sent by the client  

- **401 Unauthorized**
  - Authentication is required to access the resource  

- **403 Forbidden**
  - Access denied, even with authentication  

- **404 Not Found**
  - Requested resource does not exist  

- **500 Internal Server Error**
  - Generic server-side error  

- **503 Service Unavailable**
  - Server temporarily unavailable (down for maintenance or overloaded)

## 🧪 TryHackMe Lab Example (HTTP Status Codes)
- Explored HTTP response status codes using an interactive website  

### Tasks Performed:
- Viewed different HTTP status codes in a browser  
- Observed how servers respond to requests with specific codes  
- Used a visual tool (http.cat) to understand status code meanings  

### Key Observations:
- Status codes help diagnose issues in web communication  
- HTTP status codes provide quick insight into whether a request was successful or failed  

💡 Understanding status codes helps identify abnormal behaviour, such as repeated errors or failed requests during attacks  

## 🛠️ Practical Skills Developed
- Interpreting HTTP status codes during web browsing and testing  
- Analysing server responses to identify issues  
- Recognising patterns in client-side and server-side errors  

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  

## 🔐 Security Relevance
- **Status codes** are heavily used in security testing and monitoring   

## 📌 Lessons Learned  
⚠️ Status codes provide critical feedback about the outcome of requests  
⚠️ Different categories indicate where an issue originates (client vs server)  
⚠️ Understanding status codes is essential for troubleshooting and security analysis       