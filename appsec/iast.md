# IAST
Interactive Application Security Testing is the process of instrumenting runtime code to identify and report security vulnerabilities. Agents specific to each programming language run alongside the application to monitor traffic and scan application runtime code to detect vulnerabilities and report them to the central server.

Organizations small and medium who are looking for simple, effective and quick security solution that encompases features of SAST, DAST and OSS. IAST is a perfect solution as the onboarding, setup and maintenance is less. While also providing effective results.

### Benefits
 - As agents have direct  access to runtime source code and traffic they are in a better position to identify true positives compared to SAST. 
 - Also agents can scan to identify runtime dependencies to identify true positive OSS vulnerabilities. 
 - As agents can be added to application in lower environments and even local developer machines they can be utilized to achieve early detection and DevSecOps
 - 
## How to integrate

 - IAST client agents should be initialized during application startup in lower level environments in continuous monitor mode.
 - IAST tools can be configured to report issues directly to application ticketing systems to manage and remediate security issues
 - IAST agents can be also utilized with IDE's to help identify issues with local development.
 - The are many options available ranging from IDE, Maven, Gradle, Docker and other options to plugin agents to your runtime.
 - 

## IAST Tools
[open source security tools](https://owasp.org/www-community/Free_for_Open_Source_Application_Security_Tools)

### Considerations
 - IAST agents typically have a minor performance impact so important to evaluate them for your technology stack.
 - Its critical to setup automation to keep agents and policies up to date to produce effective results. 
 - We have noticed issues with agents having issues with some technology stacks.

### Tidbit
 - When the Log4j CVE were published IAST tools were utilized to identify all applications using the vulnerable library and remediate them.
 





