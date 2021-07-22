# Level (hazard level)
> The vulnerability level definition is recommended to be determined by the maximum hazard of the vulnerability.

| Level | Score | Description |
|--|--|--|--|
| Critical | 9-10 | 1. Can obtain server privileges; 2. Severe Information leakage; |
| High risk | 6-8 | 1. Sensitive Information leakage; 2. Overstepping privileges; 3. Arbitrary file reading; 4. SQL injection; 5. git/svn leakage; 6. SSRF;|
| Medium risk | 3-5 | 1.XSS; 2.URL jumping; 3.CRLF; 4.LFI;|
| Low Risk | 1-2 | 1.CSRF; 2.JSONP hijacking; 3.Exceptional stack information; 3.PHPINFO; 4.Path leakage; 5.Hardcoded passwords; 6.Hardcoded intranet IP domains; 7.Insecure encryption methods; 8.Insecure random numbers; 9.Log sensitive records;|

--
Next chapter: [Program directory structure](http://cobra.feei.cn/tree)
