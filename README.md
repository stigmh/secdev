# Security resources for developers

"The ultimate" collection of security resources and tools for secure development, secure coding and DevSecOps. Contributions (PRs) are appreciated.

## Litterature

- OWASP Top 10 (**Updated 2021**)
    * https://owasp.org/Top10/
    * Don’t just know about it, learn the actual contents!
- OWASP Top 10 for APIs
    * https://owasp.org/www-project-api-security/
- OWASP Top 10 for mobile
    * https://owasp.org/www-project-mobile-top-10/
- OWASP cheat sheets
    * Best developer security practices for “everything!”
    * https://cheatsheetseries.owasp.org/
    * Examples:
        - Best practice for file uploads: https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html
        - Best practice for input validation: https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html
        - JavaScript third-party (dependency) management: https://cheatsheetseries.owasp.org/cheatsheets/Third_Party_Javascript_Management_Cheat_Sheet.html
        - CWE/SANS Top 25 Most Dangerous Software Errors
            - https://www.sans.org/top25-software-errors/
- Department of Defense (DoD) Enterprise DevSecOps Initiative
    * https://software.af.mil/dsop/documents/
- [Security Champions Playbook](https://github.com/c0rdis/security-champions-playbook)
- Books
    * [OWASP Code Review Guide v2 (2017)](https://owasp.org/www-project-code-review-guide/assets/OWASP_Code_Review_Guide_v2.pdf)
        - Free **must read** for every developer
        - [Project page](https://owasp.org/www-project-code-review-guide/)
    * [Secure Programming HOWTO - Creating Secure Software](https://dwheeler.com/secure-programs/) by _David A. Wheeler_
        - **Free** HTML and PDF book by the author of [Flawfinder](https://pypi.org/project/flawfinder/)
    * [The Art of Software Security Assessment](https://www.amazon.com/Art-Software-Security-Assessment-Vulnerabilities-ebook-dp-B004XVIWU2/dp/B004XVIWU2/) by _John McDonald_, _Mark Down_ and _Justin Schuh_
        - As recommended by _Natalie Silvanovich_ at [Google Project Zero](https://googleprojectzero.blogspot.com)
        - Note **only ebook** is the complete version for some reason
   * [A Bug Hunter's Diary](https://www.amazon.com/Bug-Hunters-Diary-Software-Security-ebook/dp/B00652XO2I/) by _Tobias Klein_
- Articles
    * [How to prevent, detect and respond to cloud token theft](https://www.microsoft.com/en-us/security/blog/2022/11/16/token-tactics-how-to-prevent-detect-and-respond-to-cloud-token-theft/) (Session hijacking of cloud access token)
    * [SVGs are dangerous](https://web.archive.org/web/20220416143159/https://www.mnemonic.no/blog/exploiting-scratch-with-a-malicious-image/). How an XSS vulnerability in an electron application can lead to remote code execution.
- [Equinor AppSec information pages](https://appsec.equinor.com/)
- [NAV's security playbook](https://sikkerhet.nav.no/) (Norwegian)

## Interactive training

- Learn OWASP Top 10 (2017 edition) interactive with WebGoat (free)
    * https://owasp.org/www-project-webgoat/
- OWASP Secure Coding Dojo (free) interactive secure coding training
    * https://securecodingdojo.owasp.org/
    * Project page with self-hosting & workshop resources:
        - https://owasp.org/www-project-secure-coding-dojo/
- TryHackMe (some rooms are free) interactive tutorials of various topics
    * https://tryhackme.com/
- PortSwigger Web Security Academy (free) interactive online web sec. training
    * https://portswigger.net/web-security
- Free API Security class & certification based on OWASP API Security Top 10
    * https://university.apisec.ai/apisec-certified-expert
- OWASP Juice Shop (free) intentionally vulnerable application
    * https://owasp.org/www-project-juice-shop/
- Practice cloud security with AzureGoat and AwsGoat
    * https://github.com/ine-labs/AWSGoat (AWS)
    * https://github.com/ine-labs/AzureGoat (Azure)

## Tools

- Analyze and test your HTTP Security Headers
    * https://securityheaders.com/ (free)
- Analyze and test your TLS/SSL configuration
    * https://www.ssllabs.com/ssltest/ (free)
    * https://github.com/drwetter/testssl.sh (free)
- (Web) Vulnerability scanners
    * Nikto (free)
        - https://github.com/sullo/nikto
    * Trivy (free)
        - https://trivy.dev/
    * Greenbone Community Edition (previously OpenVAS) (free)
        - https://greenbone.github.io/docs/latest/index.html
    * Nessus
        - https://www.tenable.com/products/nessus
- Static Application Security Testing (SAST)
   - OWASP Source Code Analysis Tools
      - https://owasp.org/www-community/Source_Code_Analysis_Tools
   - NIST’s list of SAST tools you can integrate in your DevSecOps pipeline:
      - https://www.nist.gov/itl/ssd/software-quality-group/source-code-security-analyzers
   - Semgrep (commercial)
      - https://semgrep.dev/products/semgrep-code/
   - Snyk Code (commercial)
      - https://snyk.io/product/snyk-code/
   - Sonarcube (commercial)
      - https://www.sonarsource.com/products/sonarqube/
   - Flawfinder
      - https://pypi.org/project/flawfinder/
- Commercial DevSecOps vulnerability scanners
    - https://www.sonarqube.org/
    - https://snyk.io/product/snyk-code/
- “Attack proxies” for web analysis and attacks:
    - OWASP Zap Proxy (free)
        * https://www.zaproxy.org/
    - Portswigger Burp Suite (free limited version available)
        * https://portswigger.net/burp
    - Hetty (free)
        * https://hetty.xyz/
- Privacy tools / alternatives to popular products
    - https://www.privacytools.io/

## Communities

- [DevSecOps Book Club](https://dsobook.club/)
- [/r/netsec](https://old.reddit.com/r/netsec/)
- [Security Champions Norge](https://securitychampions.no/) (Norwegian)

## Technology specific

### Third-party dependency vulnerability scans

### dotnet

Find vulnerable packages:

```
dotnet list package --vulnerable --include-transitive
```

Outdated packages:

```
dotnet list package --outdated
```

### Java

Use [OWASP Dependency-Check](https://owasp.org/www-project-dependency-check/)

### python

Find vulnerable dependencies with [pip-audit](https://pypi.org/project/pip-audit/)

### nodejs / npm

Check for third-party (dependencies) vulnerabilities:

```
npm audit
```

Only production packages:

```
npm audit --omit=dev
```

### rust

Use [cargo-audit](https://crates.io/crates/cargo-audit)

### go

Use [govulncheck](https://pkg.go.dev/golang.org/x/vuln/cmd/govulncheck).

## Other lists

- https://github.com/sbilly/awesome-security

