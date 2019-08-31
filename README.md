# Opencart 3.x.x Authenticated Stored XSS
# CVE-2019-15081

### Description

The Opencart Version 3.x.x allows editing Source/HTML of the Categories / Product / Information pages in the admin panel which isn't sanitized to user input allowing for an attacker to execute arbitrary javascript code leading to Stored Cross-Site-Scripting(XSS).

### CVE-2019-15081 Proof-of-Concept(POC)

1. Log-in to admin-panel.

2. Navigate to **Catlog** and then **Categories** or **Products** or **Information** and select any.

3. Under description click on **Source** option and insert your XSS payload. i.e: "><script>alert("XSS")</script>
![Opencart Authenticated Stored XSS](/oc_authenticated_stored_xss.png)

4. Now visit the modified page of your public website. And your injected XSS payload will execute.

![Opencart Authenticated Stored XSS](/xss_popup.png)
