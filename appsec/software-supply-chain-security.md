## Software Supply Chain Security (SSC)

Given the criticality of vulnarabilities like XZ Utils, Solarwinds and Log4j this article try's to shed light on Software Supply Chain Security background and review options for organaizations to secure against them.

## What is Software Supply Chain Security
SSC represents the lifecycle of software code, dependencies, build and deployment. Given the wide array of open source software dependencies that are embdeeded into software deployed and running across the world. Its imparative to understand various stages and ensure there are enough preventative measure at each step there by ensuring security in SSC.

![Software Supply Chain Security Phases](https://www.opensourcerers.org/wp-content/uploads/2023/07/Screenshot-2023-07-17-at-07.40.22.png)

## Phases of SSC

### Code Phase

#### Protecting Source Code Repository
This is the criticaly entry point that was used to inject malicious code for the recent attacks. So its imperative to ensure only proper authentication and authorization controls are present for the source code repository.
At a minimal ensure only valid users have access to checkin and make changes to the repos that are intented to.

#### Secure code review for source code changes.

There is also a chance that a insider with malicious intent can create a backdoor or vulnarabile code. So its critical to ensure all code changes go through a code review where its reviewed by peer before its being shipped.

#### Artifact Repository

Ensure there is a proper validation process to vet open source dependencies that can be used for your organazation.
Setting up a Artifact Repository that will only serve vetted open source dependencies that are constantly scanned for vulnarabilities and developers can only download dependencies from this will help secure SCA libraries.


### Build Phase
Compromised build platform can let untrusted code to sneak into the package. Ensuring build pipeline employes same level of protection with source code so its not tampered.

### Package and Distribute Phase
Once the software deployable package is built and ready to be distributed there should be controls to ensure the package cannot be updated with any malicious packages. This is referred as build package integrity.







