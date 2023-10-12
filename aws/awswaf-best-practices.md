#### What does WAF protect at a high level
 - Distributed denial of service (DDoS) attacks 
 - Web application attacks (App Exploits, XSS, SQLi, CVE)
 - Bots (Bots, Scrappers, Crawlers)

## Commons configurations

### Managed Rule Sets

AWS Managed Rules for AWS WAF is a set of AWS WAF rules curated and maintained by the AWS Threat
Research Team that provides protection against common application vulnerabilities or other unwanted
traffic, without having to write your own rules. You can select and add some of the AWS managed rule
groups to protect your application from various threats.

Baseline rule groups  Cover some of the common threats and security risks described in the OWASP
Top 10 publication.

Use-case specific rule groups – Provide incremental protection based on your application
characteristics, such as the application OS or database.

IP reputation rule groups – An IP reputation list derived from the Amazon threat intelligence team
blocks known malicious IP addresses.


### Rate-Based Rules
Implement rate-based rules to protect against DDoS attacks and other types of high-traffic anomalies.

### Geographic Rules:

Utilize geographic rules to block traffic from specific countries or regions if your application does not have a global audience.


## Deployment Practices
#### Test Before Deploying to Production
Once you’ve tested the WAF implementation and verified it works in the staging environment, you can determine when to deploy it to the production environment. Choose the date and time you expect to have the least user traffic. The security and application development teams should evaluate your operational readiness before deploying the implementation. Consider rollback procedures and ensure the dashboards have properly configured metrics and alerts.

Create an incident response runbook to explain how your teams can perform rollbacks and additional mitigation tasks. Ensure every team member knows how to respond to security threats, including implementing configuration updates, deploying in different accounts, troubleshooting problems, and remediating threats. The runbook should outline all the steps your teams should take.

#### Deploy AWS WAF Using Count Mode
Count mode is an option in AWS WAF that reports the number of web requests that would be blocked by your rules, but does not actually block them. This is a good way to understand the production impact of your rules before turning them on.

Once you’ve established operational readiness, you can deploy AWS WAF for the production endpoints you want to protect. Choose which rules you want to trial first and use count mode to identify false positives in the production environment that might not have appeared in the staging environment. This approach helps you ensure legitimate traffic flows smoothly, especially when deploying WAF rules for the first time.

Note that the application may be vulnerable to an attack that the rule in count mode would otherwise block. You only ensure real protection when you push the rule block mode. If you are confident in the rule’s efficacy and don’t expect many false positives, you might not want to trial rules in production.

When using count mode, review your dashboards and metrics to verify that rules match their intended purpose. Once you see the rules operated correctly, switch them to block mode.

#### Conduct Post Deployment Evaluations
Periodically monitor and review the application after you deploy AWS WAF. At this stage, security and development teams should regularly review dashboards to establish a baseline of normal application traffic. You can leverage AWS WAF logs alongside tools like Athena, OpenSearch Service, and external SIEM solutions to analyze traffic patterns and identify potentially threatening changes.

These tools provide detailed information to help you understand anomalies, detect new threats, or recognize false alarms. Review your runbook to keep it up to date. Practice the runbook regularly to see how well it performs and let team members familiarize themselves with security response procedures.

Regular penetration testing is another useful way to keep up with emerging threats and address zero-day vulnerabilities. Keep your WAF rules current to ensure they protect your application against the latest threats. Using managed rules will help you reduce the technical effort required to keep your WAF up to date. AWS and third-party WAF providers regularly update managed rules—however, you should also proactively upgrade your custom or application-specific WAF rules.