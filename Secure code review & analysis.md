Code review can be done manually or automated.
Static analysis examines the source code without executing the program. In contrast, Dynamic analysis looks at the source
code when the program is running, static analysis detects bugs at the implementation level, and dynamic analysis detects errors during program runtime.
## SAST

SAST means **Static Application Security Testing**, a **white box** testing method that directly analyses the source code.

Many people tend to develop an application that could automate or execute processes quickly and improve performance and user experience, thereby forgetting the negative impact an application that lacks security could cause.
## SCA
SCA is used to scan dependencies for security vulnerabilities, helping development teams track and analyse any open-source component brought into a project. SCA is now an essential pillar in security testing as modern applications are increasingly composed of open-source code. Nowadays, one of the biggest challenges developer teams have is ensuring their codebase is secure as applications are assembled from different building blocks.
## DAST

DAST means **Dynamic Application Security Testing**, a **black-box** testing method that finds vulnerabilities at runtime. DAST is a tool to scan any web application to find security vulnerabilities. This tool is used to detect vulnerabilities inside a web application that has been deployed to production. DAST tools will always send alerts to the security team assigned for immediate remediation.it conducts its vulnerability assessment outside as it does not have access to the application source code. DAST is typically used during the testing phase of SDLC.
## IAST
IAST means **Interactive Application Security Testing** that analyses code for security vulnerabilities while the app is running. It is usually deployed side by side with the main application on the application server. IAST is an application security tool designed for web and mobile applications to detect and report issues even while running. IAST was developed to stop all the limitations in both SAST and DAST. It uses the Grey Box Testing Methodology.
### **How Does IAST Work**
IAST testing occurs in real-time, just like DAST, while the application runs in the staging environment. IAST can identify the line of code causing security issues and quickly inform the developer for immediate remediation. IAST checks the source code similar to SAST, but at the post-build stage, unlike SAST, which occurs during development. IAST agents are typically deployed on the application servers. When the DAST scanner performs its work by reporting a vulnerability, the deployed IAST agent will now return a line number of the issue from the source code. During functional testing performed by a QA tester, the agent studies every pattern that a data transfer inside the application follows regardless of whether it's dangerous. For example, if data is coming from a user and the user wants to perform an SQL Injection on the application by appending an SQL query to a request, the request will be flagged as dangerous.

## RASP
"RASP" stands for Runtime Application Self Protection. RASP is a runtime application integrated into an application to analyse inward and outward traffic and end-user behavioural patterns to prevent security attacks. This tool is different from the other tools as RASP is used after product release, making it a more security-focused tool when compared to the others that are known for testing.
### **How does RASP work** 
RASP is deployed to a web or application server next to the main application while running to monitor and analyse the inward and outward traffic behaviour. Immediately once an issue is found, RASP will send alerts to the security team and immediately block access to the individual making a request. When you deploy RASP, it will secure the whole application against different attacks. It does not just wait or try to rely only on specific signatures of some known vulnerabilities.

RASP is a complete solution that observes every detail of different attacks on your application and knows your application behaviour.

## Choosing tools
SAST, DAST, and IAST are great tools that complement each other. A key strength of DAST is that it identifies runtime issues—weaknesses that aren't discoverable when an application isn't running. SAST is excellent at identifying vulnerabilities while code is being written. Additionally, DAST looks at how an application responds to an attack, providing helpful insight into how likely it would be for that vulnerability to be manipulated. AST enables DevSecOps and supports continuous testing, monitoring, assessment, and validation in real-time. IAST helps prioritise and alert on vital critical risks, as defined by business goals and application security needs. For example, if choosing SAST, you can integrate it when engineers push code, and they can get feedback on the PR before merging.
![[Pasted image 20240909123555.png]]