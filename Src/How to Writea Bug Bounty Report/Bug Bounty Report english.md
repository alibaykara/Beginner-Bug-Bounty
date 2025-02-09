### How to Write a Bug Bounty Report

When participating in a bug bounty program, clear and concise reporting is key to ensure your findings are acknowledged and rewarded. Here's a step-by-step guide on how to write an effective bug bounty report:

#### 1. **Title**
   - Keep it short but descriptive. Example: `Stored XSS on User Profile Page`.

#### 2. **Description**
   - Provide a detailed description of the vulnerability. 
   - What is the issue? Where is it located (e.g., URL or feature name)? 
   - Why is it a problem? 

   Example:
   - **Issue**: A stored cross-site scripting (XSS) vulnerability is present in the user profile page.
   - **Location**: https://example.com/user/profile
   - **Impact**: An attacker can inject JavaScript code into the profile bio field, leading to potential session hijacking or defacement.

#### 3. **Steps to Reproduce**
   - List the exact steps to reproduce the vulnerability.
   - Be as clear and precise as possible to help the program maintainers reproduce the issue.
   
   Example:
   1. Go to the user profile page: `https://example.com/user/profile`
   2. In the "Bio" field, inject the following payload: `<script>alert('XSS')</script>`
   3. Save the profile.
   4. Reload the page and the JavaScript payload will execute.

#### 4. **Proof of Concept (PoC)**
   - Attach any relevant screenshots, videos, or other proof that demonstrates the vulnerability.
   - If the vulnerability involves code execution, provide the exact payload.

   Example:
   - [Screenshot showing injected payload]
   - [Video showing exploit in action]

#### 5. **Expected Behavior**
   - Describe what should happen in a secure version of the application.
   - Example: "The bio field should sanitize all user inputs to prevent script execution."

#### 6. **Actual Behavior**
   - Explain how the vulnerability manifests. 
   - Example: "The JavaScript payload executes upon reloading the page, allowing an attacker to perform actions on behalf of the victim."

#### 7. **Impact Assessment**
   - Describe the potential impact of the vulnerability, including any possible exploits.
   - Example: "An attacker could steal the user's session cookie, leading to account compromise."

#### 8. **Remediation Suggestions**
   - Offer suggestions for fixing the vulnerability, if possible.
   - Example: "Sanitize all user input on the server-side to prevent malicious script execution."

#### 9. **References**
   - Include any relevant documentation or links (e.g., OWASP recommendations, CVE entries).
   - Example: [OWASP XSS Cheat Sheet](https://github.com/OWASP/www-community/blob/master/pages/attacks/Cross-site-Scripting-(XSS).md)

---

This structure helps ensure that your report is clear, actionable, and professional, increasing the chances of it being resolved quickly and accurately. Happy hunting!
