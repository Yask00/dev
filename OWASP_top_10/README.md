# OWASP – Open Web Application Security Project

[Prevent XSS](https://cheatsheetseries.owasp.org/cheatsheets/Cross_Site_Scripting_Prevention_Cheat_Sheet.html)

[Test hacking](https://google-gruyere.appspot.com/)

### Injection:
- Untrusted data send to server as part of command or query
- Data can be stolen, modified or deleted
- Prevent via sanitize input data, penetrate tests, latest frameworks
- Most common is SQL injection

### Broken Authentication and Session Management:
- Incorrectly build auth and session man. Scheme that allows attacker to impersonate another user
- Attacker can take identity
- Don’t develop you own authentication schemes, use good frameworks, require current credentials on sensitive request, use multifactor authentication, expire session after x time, be careful with remember me functionality

### Cross Site Scripting XSS:
- Untrusted user input is interpreted by browser and executed
- Hijack user session, deface web sites, change content
- Escape untrusted data input, latest UI frameworks


### Broken Access Control:
- Restrictions on what authenticated user are is allow to do
- Attacker can access data sensitive
- Check access on UI level and server level, deny access by default

### Security Misconfiguration:
- Human mistake of misconfiguration the system, f.e. default password of webcam
- Depends on the config
- Prevent via change default credentials, turn off defaults, updating scan and audit the system

### Sensitive Data Exposure:
- Exposed data like passwords, security number
- Data is lost, corrupted
- Always obscure data, update cryptographic algorithms (MD5, DES, SHA-0, SHA-1 are secured)Use salted encryption on storage of passwords

### Insufficient Attack Protection:
- Apps that are attacked but don’t recognize the attack, letting it happen again and again
- Leak of data, decrease app availability
- Detect the log for abnormals, block them users or Ips and patch it

### CSRF Cross site request forgery:
- Forces victim to execute unwanted actions and app in which they’re authenticated
- Reauthenticate for critical actions, include hidden token in request and use frameworks with enabled CSRF protection

### Using components with KNOWN Vulnerabilities:
- 3rd party comps that the focal system uses (e.g. auth framework)
- Range from subtle to bad impact
- Always stay current with frameworks and follow best practices for virtual patching

### Underprotected APIs
- Often API are unprotected, can impact data theft, unauth access or corruption
- Secure communication between server/client, reject invalid input, latest FW, use penetration testers and code reviewers

### XML external entities – 2017
- Older or poorly config XML processors evaluate external entity references within XML docs
- Causes extraction of data, remote code execution and DDos
- Use JSON, avoid serialization of sensitive data, upgrade XML processors, enable whitelisting..

### Insecure deserialization – 2017
- Error in translation btw 2 objects
- Remote code exec, DDos
- Validate input user, digital signatures or serialize objects, restrict usage, monitor log

### Insufficient logging and monitoring - 2017
- Not able to discover an attack 
- Allow attacker to persist extract and destroy data
- Log login, access control and server side input validation

### Cryptographic failures – 2021
- Ineffective execution and config of cryptography (FTP, HTTP, MD5, WEP)
- Sensitive data exposed
- Never roll own crypto, tools to analyze, key management

### Insecure Design – 2021
- Using security by design causes breach of confidentiality.

### Software and data Integrity – 2021
- App relies on update from trusted source, but that is compromised. Supply chain attack, data exfiltration, ransomware. - Verify input through digital signature, check for vulnerabilities..

### Server side request forgery – 2021
- Not validating user supplied URL, attacker can access data. Sanitize and validate input, listening ports on connection.
