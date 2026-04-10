# Web Fundamentals – TryHackMe and Solent University Cybersecurity Coursework 

Platform: TryHackMe   
Level: Beginner / Foundation  
Focus Area: Cookies

## 🎯 Objective 
- Understand what cookies are and how they are used in web applications  
- Learn how cookies maintain state between client and server  
- Identify common uses of cookies such as sessions, preferences, and tracking  
- Understand how cookies are transmitted using HTTP headers  
- Recognise the security risks associated with cookies  

## 🧠 Core Concepts Learned 

## Cookies
- Cookies are small pieces of data stored by the browser on the client’s device  
- Cookies are set by the server using the **Set-Cookie** header  
- The browser automatically sends cookies back to the server in future requests using the **Cookie** header   

## Common Uses of Cookies
- **Login Sessions:**
  - Allow users to stay authenticated without logging in on every page  

- **Preferances:**
   - Store settings such as language, theme, dark mode settings

- **Shopping Cart:** 
  - Keep track of selected items across multiple pages  

- **Tracking:**
  - Used for analytics, advertising, and user behaviour monitoring  

## 🛠️ Practical Skills Developed
- Identifying cookies in browser developer tools  
- Understanding how cookies are sent and received via HTTP headers  
- Analysing how sessions are maintained in web applications     

## 🧰 Tools Used 
- Solent University Cybersecurity Coursework 
- TryHackMe platform  

## 🔐 Security Relevance
- Cookies are often used to store **session identifiers**, making them a target for attackers  
- If intercepted, cookies can be used in **session hijacking attacks**   
- Improperly configured cookies can expose sensitive user data     

## 📌 Lessons Learned  
⚠️ They are essential for authentication and user experience  
⚠️ Improper handling of cookies can lead to serious security vulnerabilities  