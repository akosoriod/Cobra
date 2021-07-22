# Labels
> Labels are used to label the type of vulnerability to which the scan rule belongs.

| ID | Label | Description(EN) | Description(CN) |
|--|--|--|--|--|
| 110 | MS | Misconfiguration | Misconfiguration |
| 120 | SSRF | Server-Side Forge | Server-side forgery |
| 130 | HCP | Hard-coded Password | Hard-coded Password |
| 140 | XSS | Cross-Site Script | Cross-Site Scripting |
| 150 | CSRF | Cross-Site Request Forge | Cross-Site Request Forgery |
| 160 | SQLI | SQL Injection | SQL Injection
| 163 | XI | Xpath Injection | Xpath Injection
| 165 | LI | LDAP Injection | LDAP Injection
| 167 | XEI| XML External Entity Injection | XML Entity Injection |
| 170 | FI | Local/Remote File Inclusion | File Inclusion Vulnerability
| 180 | CI | Code Injection | Code Injection
| 181 | CI | Command Injection | Command Injection
| 190 | IE | Information Exposure | Information leakage |
| 200 | PPG | Predictable Pseudorandom Generator | Predictable Pseudorandom Generator
| 210 | UR | Unvalidated Redirect | Unvalidated Arbitrary Link Bounce |
| 220 | HRS | HTTP Response Splitting | HTTP Response Splitting |
| 230 | SF | Session Fixation | SESSION fixation |
| 260 | US | unSerialize | Deserialization Vulnerability
| 280 | DF | Deprecated Function | deprecated function |
| 290 | LB | Logic Bug | Logic Bug
| 320 | VO | Variables Override | Variable Override Vulnerability
| 350 | WF | Weak Function | Insecure Function |
| 355 | WE | Weak Encryption | Insecure Encryption |
| 360 | WS | WebShell | WebShell |
| 970 | AV | Android Vulnerabilities | Android Vulnerabilities |
| 980 | IV | iOS Vulnerabilities | iOS Vulnerabilities
| 999 | IC | Insecure Components | Reference to a vulnerable three-party component (Maven/Pods/PIP/NPM) |

## Label development specification
- The first and second digits of the ID are overlaid on a base of 10 for large categories and the third digit of the ID is overlaid on a base of 2 for small categories.
- Label abbreviations by default use the initials of the description, up to four characters.
- After editing, please modify the corresponding `rules/vulnerabilities.xml`

---
Next chapter: [Hazard Class Definition](http://cobra.feei.cn/level)
