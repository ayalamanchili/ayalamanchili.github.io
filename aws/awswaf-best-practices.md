#### Below are the main categories of attacks that WAF provides protection for
 - Distributed denial of service (DDoS) attacks 
 - Web application attacks (App Exploits, XSS, SQLi, CVE)
 - Bots (Bots, Scrappers, Crawlers)

## Common configuration

### Managed Rule Sets

These are **AWS managed rules** curated and maintained by the AWS Threat
Research Team that provides protection against common application vulnerabilities (OWASP etc) or other unwanted traffic, without having to write your own rules. You can select and add some of the AWS managed rulegroups to protect your application from various threats.

**Use-case specific rule groups** provide incremental protection based on your application characteristics, such as the application OS or database.

Finally there are **IP reputation rule groups** managed by the Amazon threat intelligence team blocks known malicious IP addresses.


### Rate-Based Rules
Depending upon your application needs and user traffic you can add rate limits to protect against DDoS attacks and other types of high-traffic anomalies.

### Geographic Rules:

If you application and data needs to be restricted to certain locations you can add  rules to block traffic from specific countries.



## Deployment Best Practices
Below are the some best practices that can be utilized for effective WAF security while reducing risk of application availability issues.

* Identify and Implement WAF in a lower envirment like staging/UAT/PreProd.
* Turn on your rules in count mode (this will not block) so it will help you to identify if any legitemate application requests will be clocked in production.
* Run regression tests and test traffic for observation for like 2 weeks etc to identify and rules that are causing issues with legitimate traffic.
* Tune rules if they are blocking any legitimate application traffic.
* After tuning and validation in lower env promote the WAF config/rules to prod again in count mode. (This step is important as for some application there will still be cases where some legit prod traffic that will be blocked that needs tuning)
* After monitoring for period in prod and your team is comfortable update the rules to block mode.
* Setup a recurring review sessions to monitor and review the application. At this stage, security and development teams should regularly review dashboards to establish a baseline of normal application traffic. You can leverage AWS WAF logs alongside tools like Athena, OpenSearch Service, and external SIEM solutions to analyze traffic patterns and identify potentially threatening changes.


