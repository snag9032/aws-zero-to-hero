#### INSTRUCTOR DETAILS

|  Information             | Details                                                                      |
|----------------------    |------------------------------------------------------------------------------|
| **Name**                 | Moole Muralidhara Reddy                                                      |
| **Email**                | techworldwithmurali@gmail.com                                                |
| **Website**              | https://www.techworldwithmurali.com               |
| **LinkedIn profile**     | [Moole Muralidhara Reddy](https://www.linkedin.com/in/moole-muralidhara-reddy) |

### What is AWS WAF?

- AWS WAF (Web Application Firewall) is a security service from AWS that protects your website or web app from common online threats like hackers, bots, and malicious traffic, which could slow down your app, expose sensitive data, or use up too many resources.
- It allows you to control which traffic to allow or block to your web applications by defining customizable web security rules.
  
## What it Protects

- **Amazon CloudFront distributions**
- **Amazon API Gateway REST APIs**
- **Application Load Balancers**
- **AWS AppSync GraphQL APIs**
- **Amazon Cognito user pools**
- **AWS App Runner services**
- **AWS Verified Access instances**

  
### Key Features of AWS WAF:

1. **Managed Rulesets**:
   - AWS WAF provides managed rulesets that include pre-configured rules to protect against common threats such as SQL injection, cross-site scripting (XSS), and known bad bots.
   - These rulesets are regularly updated to include new protections.

2. **Customizable Rules**:
   - You can create custom rules to define specific conditions under which the AWS WAF should allow, block, or monitor web requests.
   - These rules can be based on IP addresses, HTTP headers, URI strings, or combinations thereof.

3. **Integration with AWS Services**:
   - AWS WAF integrates seamlessly with other AWS services like Amazon CloudFront (CDN), Application Load Balancer (ALB), API Gateway, and AWS AppSync, allowing you to protect applications deployed on these services.

4. **Monitoring and Logging**:
   - AWS WAF provides metrics and logs through AWS CloudWatch, giving you visibility into web traffic patterns and potential security threats.
   - You can set up alarms based on these metrics to alert you to potential attacks.

5. **Scalability and Performance**:
   - AWS WAF automatically scales with your application traffic and provides low-latency performance by leveraging AWS's global network of edge locations.

6. **Rate Limiting and Bot Control**:
   - You can configure rate-based rules to protect against application-layer attacks such as brute force login attempts or HTTP floods. AWS WAF also includes bot control features to identify and mitigate automated threats.

----
#### Creating and Managing Web ACLs in AWS WAF

1. **Sign in to AWS Management Console:**
   - Navigate to the AWS WAF & Shield Dashboard at [AWS Management Console](https://console.aws.amazon.com/wafv2/).

2. **Create a Web ACL:**
   - Click on "Create Web ACL."
   - Enter a name and description for your Web ACL.
   - Define rules using conditions (e.g., IP addresses, HTTP headers, URI strings).
   - Add rules to the Web ACL and configure actions (allow, block, count, etc.) based on rule matches.
   - Click "Create" to create the Web ACL.
----
#### Applying a Web ACL to an Application Load Balancer (ALB)

1. **Sign in to AWS Management Console:**
   - Navigate to the AWS WAF & Shield Dashboard at [AWS Management Console](https://console.aws.amazon.com/wafv2/).

2. **Select Web ACL:**
   - Choose the Web ACL you created or want to apply.

3. **Associate with ALB:**
   - Click on "Associations" in the left-hand navigation pane.
   - Click "Add association" to associate the Web ACL with your Application Load Balancer (ALB).
   - Select the ALB and configure the association settings.
   - Save the association to apply the Web ACL to the ALB.
----

List of commonly used **AWS-managed rule groups** for real-time protection:  

### **1. AWS Core Rule Set (CRS)**  
✔ Protects against common OWASP Top 10 threats, such as:  
   - SQL Injection (SQLi)  
   - Cross-Site Scripting (XSS)  
   - Command Injection  
   - Local File Inclusion (LFI)  
   - HTTP Protocol Violations  

✅ **Use Case:** General web application security  

---

### **2. AWS Known Bad Inputs Rule Set**  
✔ Blocks known attack patterns, including:  
   - Common malicious payloads  
   - Exploits targeting web applications  
   - Attempts to manipulate parameters  

✅ **Use Case:** Protects against frequently observed threats  

---

### **3. AWS SQL Injection Rule Set**  
✔ Detects and blocks SQL injection attempts in:  
   - Query strings  
   - POST bodies  
   - HTTP headers  

✅ **Use Case:** Prevents database-related attacks  

---

### **4. AWS XSS Rule Set**  
✔ Detects and blocks **Cross-Site Scripting (XSS)** attacks in:  
   - User inputs  
   - Web forms  
   - HTTP headers  

✅ **Use Case:** Prevents browser-based security vulnerabilities  

---

### **5. AWS IP Reputation List Rule Set**  
✔ Blocks requests from **known malicious IPs** based on AWS threat intelligence.  

✅ **Use Case:** Mitigates attacks from bad actors, bots, and compromised servers  

---

### **6. AWS Anonymous IP List Rule Set**  
✔ Blocks traffic from:  
   - VPNs  
   - Tor exit nodes  
   - Proxy servers  
✅ **Use Case:** Prevents traffic from anonymized sources often used by attackers  

---

### **7. AWS Bot Control Rule Set**  
✔ Detects and mitigates bot traffic using:  
   - **Common Bot Detection** – Blocks known bad bots  
   - **Advanced Bot Detection** – Differentiates good bots (search engines) from bad ones  
   - **CAPTCHA Challenges** – Verifies human users  

✅ **Use Case:** Prevents automated attacks like credential stuffing and scraping  

---

### **8. AWS Account Takeover Prevention (ATP) Rule Set**  
✔ Detects suspicious login activity, including:  
   - Credential stuffing  
   - Unusual login attempts  
   - Brute-force attacks  

✅ **Use Case:** Protects user accounts on login and authentication pages  

---

### **9. AWS Managed DDoS Protection Rule Set** (For AWS Shield Advanced customers)  
✔ Protects against high-volume **Layer 7 DDoS attacks**  
✔ Blocks **application-layer flood attacks**  

✅ **Use Case:** Defends against large-scale web application DDoS threats  

---

### **10. Third-Party Managed Rule Groups (AWS Marketplace)**  
✔ Available from security vendors like:  
   - **Fortinet** – Advanced web filtering and bot protection  
   - **F5** – WAF rule sets for API security  
   - **Imperva** – OWASP protection and behavioral analysis  
   - **Trend Micro** – Real-time malware and exploit blocking  

✅ **Use Case:** Industry-specific security solutions with enhanced threat intelligence  

-----
### Blocking a Specific IP Address in AWS WAF

1. **Sign in to AWS Management Console:**
   - Navigate to the AWS WAF & Shield Dashboard at [AWS Management Console](https://console.aws.amazon.com/wafv2/).

2. **Create IP Set:**
   - Go to "IP sets" in the left-hand navigation pane.
   - Click on "Create IP set."
   - Enter a name for the IP set and add the IP addresses you want to block.

3. **Create Rule to Block IP:**
   - Go to "Rules" in the left-hand navigation pane.
   - Click on "Create rule."
   - Define a condition based on IP addresses and select the IP set you created.
   - Set the action to "Block."
   - Save the rule.

4. **Associate Rule with Web ACL:**
   - Go to the Web ACL where you want to apply the rule.
   - Add the rule to the Web ACL.
   - Save the changes to apply the rule, effectively blocking the specified IP addresses.

---

### **Monitoring and Logging AWS WAF Activity**  

To monitor and log AWS WAF activity effectively, follow these key steps:  

### **1. Enabling AWS WAF Logging**  
AWS WAF allows you to log all web requests that match your defined rules. You can enable logging by:  
- Navigating to the **AWS WAF Console**  
- Selecting your **Web ACL**  
- Going to the **Logging and Metrics** section  
- Enabling logging to **Amazon Kinesis Data Firehose**, which can then send logs to **Amazon S3, Amazon CloudWatch**  

### **2. Monitoring with AWS WAF Metrics**  
AWS WAF provides built-in **CloudWatch metrics** to track:  
- **Allowed requests**  
- **Blocked requests**  
- **Counted requests**  
- **Requests per rule group**  

You can create CloudWatch **dashboards and alarms** to monitor traffic patterns and detect anomalies.  

### **3. Analyzing AWS WAF Logs**  
AWS WAF logs contain detailed request information, including:  
- **Source IP address**  
- **Country of origin**  
- **User-Agent details**  
- **Matched rule and action taken (allow/block/count)**  
