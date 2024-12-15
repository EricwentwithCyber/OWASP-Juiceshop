# OWASP-Juiceshop
Web Application Penetration Testing with OWASP Juice Shop


Why This Project?
As an aspiring penetration tester, I took on this hands-on project using OWASP Juice Shop, a vulnerable web application. 
The goal was to simulate real-world scenarios, identify, and exploit vulnerabilities in a safe and legal environment. 
This project allowed me to refine my skills and deepen my understanding of securing applications.


Project Objectives
Gain practical experience in web application penetration testing.
Complete at least two 2-star challenges, two 3-star challenges, and one 1-star challenge.
Document findings and recommend mitigations.
Tools and Environment
Tools Used: Burp Suite, Kali Linux
Testing Sites:
Online: juice-shop.herokuapp.com
Offline: localhost:3000
Challenges and Solutions


Challenge 1: Login Challenge (2-Star)
Objective: Gain unauthorized admin access.
Steps Taken: Injected SQL payload: admin’ or 1=1 --.
Findings: Authentication bypass due to improper input validation.
Mitigations: Use prepared statements and sanitize inputs.


Challenge 2: View Basket Challenge (2-Star)
Objective: Exploit shopping basket functionality.
Steps Taken: Tampered with session cookies using Burp Suite.
Findings: Lack of session token validation allowed impersonation.
Mitigations: Use secure cookies and enforce server-side access controls.


Challenge 3: Upload Size Challenge (3-Star)
Objective: Exploit file upload functionality.
Steps Taken: Modified the Content-Length header to bypass file size restrictions.
Findings: Missing server-side validation enabled DoS attacks.
Mitigations: Enforce file size restrictions and validate uploads server-side.


Challenge 4: CAPTCHA Bypass (3-Star)
Objective: Bypass CAPTCHA protection.
Steps Taken: Intercepted CAPTCHA requests and submitted the form without solving.
Findings: Weak client-side CAPTCHA validation.
Mitigations: Implement server-side CAPTCHA validation and rate-limit requests.


Challenge 5: DOM-XSS (1-Star)
Objective: Perform a DOM-based XSS attack.
Steps Taken:
Inserted the payload: <iframe src="javascript:alert('xss')">.
Observed the successful execution of the attack in the search bar.
Findings: Improper client-side handling of input allowed malicious script execution.
Mitigations: Escape special characters in user input and use CSP (Content Security Policy).


Key Learnings
The importance of validating inputs and securing cookies.
Effective server-side controls are critical for web application security.
Practical tools like Burp Suite and Kali Linux are essential for penetration testing.
