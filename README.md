# Opencart-Stored-XSS

Description :

The Opencart Version allows editing Source/HTML of the Categories / Product / Information pages in the admin panel which isn't sanitized to user input allowing for an attacker to execute arbitrary javascript code leading to Stored Cross-Site-Scripting(XSS).

Proof-of-Concept(POC):

1. Login to admin-panel

2. Navigate to **Catlog** and then **Categories** or **Products** or **Information**

3. Under description click on **Source** option and insert your XSS payload. i.e: "><script>alert("XSS")</script>
![Opencart Authenticated Stored XSS](/oc_authenticated_stored_xss.png)