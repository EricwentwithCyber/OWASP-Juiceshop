# Web Application Penetration Testing with OWASP Juice Shop

## Author
Eric Noga  
CYB505 - Introduction to Cybersecurity  

---

## Why This Project?
As an aspiring penetration tester, I wanted to challenge myself with this hands-on project to simulate a real-world scenario. Using the OWASP Juice Shop, a vulnerable web application, I identified and exploited vulnerabilities in a safe and legal environment. This project refined my skills and deepened my understanding of application security.

---

## Project Objectives

- Gain practical experience in web application penetration testing.
- Complete at least two **2-star** challenges and two **3-star** challenges.
- Document findings and recommend mitigations.

---

## Tools and Environment

### Tools
- **Burp Suite**
- **Kali Linux**

### Testing Sites
- External Testing: [juice-shop.herokuapp.com](https://juice-shop.herokuapp.com)
- Local Testing: `localhost:3000` (Offline testing)

---

## Challenges Completed

### Challenge 1: Login Challenge (2-star)
- **Objective**: Gain unauthorized admin access.
- **Steps Taken**: Used SQL Injection payload (`admin' or 1=1 --`) in the username field.
- **Findings**: Improper input validation allowed bypassing of authentication.
- **Mitigations**: Utilize prepared statements and sanitize inputs.

### Challenge 2: View Basket Challenge (2-star)
#### Part 1
- **Objective**: Exploit shopping basket functionality.
- **Steps Taken**: Tampered with session cookies using Burp Suite.

#### Part 2
- **Findings**: Lack of session token validation allowed impersonation.
- **Mitigations**: Use secure cookies and enforce server-side access controls.

### Challenge 3: Upload Size Challenge (3-star)
- **Objective**: Exploit file upload functionality.
- **Steps Taken**: Modified the `Content-Length` header to bypass file size restrictions.
- **Findings**: Missing server-side validation enabled DoS attacks.
- **Mitigations**: Enforce file size restrictions server-side and validate uploads.

### Challenge 4: CAPTCHA Bypass (3-star)
- **Objective**: Bypass CAPTCHA protection.
- **Steps Taken**: Intercepted CAPTCHA requests and submitted the form without solving it.
- **Findings**: Client-side CAPTCHA validation was weak.
- **Mitigations**: Implement server-side CAPTCHA validation and rate-limit requests.

---

## Key Takeaways
This project reinforced the importance of secure coding practices and highlighted common vulnerabilities in web applications. By applying penetration testing techniques, I gained hands-on experience and developed actionable insights to improve application security.

---

## Questions and Feedback
Feel free to reach out if you have questions or would like further insights into this project!
