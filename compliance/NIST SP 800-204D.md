### What is NIST 800-204D?
It is part of the NIST Special Publication series focused on cloud-native application security. It focuses on securing software supply chains within DevSecOps CI/CD pipelines used for cloud-native applications.

### Why is it important
 - NIST SP 800-204D serves as a roadmap for organizations to enhance security throughout the software development lifecycle (SDLC).
 - It emphasizes considering security at every step, from writing initial code to deploying the final software version2.
 - By integrating security measures into CI/CD pipelines, organizations can automate compliance, ensure artifact integrity, and enhance the overall security posture.


 ![alt text](/static/sscs-flow.png.png)

### Steps to acheive compliance with NIST 800-204D?

Key steps included in the NIST publication are.

#### General recommendations
 - Regularly applying patches and updates to software and systems to address known vulnerabilities and enhance security.
 - Capturing and managing dependencies of artifacts in a central repository to ensure they are up to date and free from vulnerabilities.
 - Implementing robust authentication mechanisms and granular authorization controls to ensure only authorized users have access to sensitive resources and functionalities
 - Implementing encryption, access controls, and data loss prevention measures to safeguard sensitive data throughout the SDLC.
 - Implementing logging, monitoring, and auditing mechanisms to detect and respond to security incidents and track changes to software artifacts and systems.
 - Ensuring compliance with relevant security standards and regulations, such as OWASP Top Ten, SP 800-53, HIPAA, and PCI DSS (industry dependent).
 - Establish trusted sources for OSS and verify digital signatures to ensure software authenticity. Even better, use internal repositories if possible.
 - Conduct regular vulnerability scans and dependency checks and audit the CI/CD processes.

 #### SevSecOps and CI/CD recommendations

 - Strengthening the execution environment (e.g., VMs or pods) minimizes the attack 
   surface, safeguarding the pipeline from potential threats.
 - Clearly establishing roles for individuals managing the CI/CD pipelines, such as 
   application updaters, package managers, and deployment specialists, ensures a structured and secure pipeline operation.
 - Implementing detailed permissions for tasks, including code generation and 
  commits, build and package generation, and artifact management within repositories, enhances security by restricting access to necessary actions only.
 - Leveraging automation tools streamlines the CI/CD pipeline, from code checkout  
   to testing phases, including Static Application Security Testing (SAST), Dynamic Application Security Testing (DAST), and Software Composition Analysis (SCA). Higher-level driver tools orchestrate these functions, operating with a higher trust level than individual steps.
 - Establishing security guidelines for different pipeline activities, from 
   application code development to deployment, including infrastructure as code and policy/configuration code, fortifies the pipeline against vulnerabilities.