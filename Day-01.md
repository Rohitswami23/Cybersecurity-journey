📅 Date: September 17, 2026

📝 Summary:
Today focused on understanding the end-to-end web penetration testing methodology through a guided scenario targeting a mock recruitment application. By mapping the application's attack surface and understanding its underlying logic, I successfully chained multiple vulnerabilities—from basic enumeration to Insecure Direct Object Reference (IDOR)—ultimately achieving full Remote Code Execution (RCE) via a file upload bypass.

🛠️ Tools & Concepts Explored:

Nmap: Introductory exposure to port scanning to identify running services (Apache on Port 80, SQL databases).

Curl: Inspected HTTP responses to identify backend technologies, such as noting PHPSESSID to confirm a PHP/Apache/SQL stack.

Gobuster: Understanding the directory brute-forcing workflow to uncover hidden administrative portals and sensitive API endpoints.

IDOR (Insecure Direct Object Reference): Exploited flawed access controls by manipulating user ID parameters (changing ID 6 to 1) to expose administrator credentials and roles.

Broken Authentication (Password Reset Flaw): Leveraged exposed API endpoints to trigger a password reset that leaked the reset token directly on the screen, allowing an admin account takeover without brute force.

File Upload Bypass: Bypassed basic server-side .php restrictions by utilizing a .phtml extension to successfully upload a web shell.

Reverse Shell: Executed commands via the uploaded web shell to connect back to a local listener, establishing full remote control over the web server.

🎯 TryHackMe Rooms Completed:
✅ Guided Pentest (Web Application Scenario)
