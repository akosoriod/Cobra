# Introduction

## What is "Source Code Security Audit (White Box Scan)"?
> Due to the varying skill levels and security awareness of developers, it is possible to develop code that has security vulnerabilities.
> Attackers can find these vulnerabilities through penetration testing, which can lead to application attacks, server intrusions, data downloads, business impacts, and other problems.
> "Source code security auditing" is the process of discovering security risks and vulnerabilities in source code through auditing, and Cobra can automate this process.

## Why can Cobra scan for vulnerabilities in source code?
> For some obvious features can use regular rules to directly match out, such as hard-coded passwords, misconfigurations, etc.
> For the OWASP Top 10 vulnerabilities, Cobra can locate all the vulnerable functions in the code by pre-sorting them and locating them based on Lex (Lexical Analyzer Generator) and Yacc (Yet Another Compiler-Compiler). ) will parse the corresponding source code into AST (Abstract Syntax Tree), and analyze whether the entry of the hazard function is controllable to determine whether there is a vulnerability (currently only PHP-AST is connected, other languages AST is connected).

## What is the difference or advantage between Cobra and other source code audit systems?
> Cobra is positioned to automate the discovery of **most notable security issues** in source code, with manual auditing recommended for some deeper hidden or unique issues.

- Development source code (based on open MIT License, source code can be changed)
- Support for many development languages (support for more than ten development languages and file types)
- Support many types of vulnerabilities (support dozens of vulnerability types)
- Support for a variety of scenarios integration (provides API can also be used on the command line)
- Professional support, continuous maintenance (continuously maintained and updated by white hats, development engineers and security engineers together, and used internally by many enterprises)

## What development languages does Cobra support?
> Cobra currently supports major development languages such as PHP, Java and dozens of other file types, and continues to update its rules and engine to support more development languages, see [Development Languages and File Types](http://cobra.feei.cn/languages) for details of support.

## What vulnerabilities does Cobra find?
> Covers most common vulnerabilities on the web side and some general vulnerabilities on the mobile side (Android, iOS), see [Vulnerability Types](http://cobra.feei.cn/labels) for support.

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
| 999 | IC | Insecure Components| referencing a vulnerable three-party component (Maven/Pods/PIP/NPM) |

## What scenarios can Cobra be used in?
1. [Before vulnerabilities appear] Daily scanning of company projects through built-in scanning rules and advancing to resolve the vulnerabilities found.
2. [After the vulnerability appears] When a new vulnerability appears, you can immediately write a Cobra scan rule to scan all company projects to determine the affected projects.

## What type of application is Cobra?
> Cobra provides web services as well as command line services.

1. [CLI] Scan local source code through command line to find security issues in it.
2. 【API&GUI】 Deployed as Web Server on the server for internal staff to access and use in the form of GUI, and can be integrated into CI or release system through API.


## How to participate in Cobra development?
> Cobra development is inseparable from the contributions of the open source community, Cobra welcomes people who have Python development experience and are interested in code auditing to join our open source community development team and contribute together (you can submit code via Pull Request, and then we invite you to join the community development group communication group).

# Cobra Documentation
- Installation
    - [Cobra Installation](http://cobra.feei.cn/installation)
- Basic usage
    - How to use CLI mode](http://cobra.feei.cn/cli)
    - How to use the API mode](http://cobra.feei.cn/api)
- Advanced use
    - [Advanced feature configuration](http://cobra.feei.cn/config)
    - [Upgrade framework and rule source](http://cobra.feei.cn/upgrade)
    - [Report module usage](http://cobra.feei.cn/report)
- Rule development specification
    - [Rule Template](http://cobra.feei.cn/rule_template)
    - [Sample Rules](http://cobra.feei.cn/rule_demo)
    - [Rules file naming specification](http://cobra.feei.cn/rule_name)
    - [Rule Development Process](http://cobra.feei.cn/rule_flow)
- Framework engine
    - [Development language and file type definitions](http://cobra.feei.cn/languages)
    - [Vulnerability type definition](http://cobra.feei.cn/labels)
    - [Hazard Level Definition](http://cobra.feei.cn/level)
    - [Program directory structure](http://cobra.feei.cn/tree)
- Contributed Code
    - [Unit Test](http://cobra.feei.cn//test)
    - [Contributors](http://cobra.feei.cn/contributors)
    - [How to contribute code?] (https://github.com/WhaleShark-Team/cobra/blob/master/CONTRIBUTING.md)
