Threat modelling is best integrated into the design phase of an SDLC before any code is written. Threat modelling is a structured process of identifying potential security threats and prioritising techniques to mitigate attacks so that data or assets that have been classified as valuable or of higher risk during risk assessment, such as confidential data, are protected. When performed early, it brings a great advantage; potential issues can be found early and solved, saving fixing costs down the line.
There are various methods to perform threat modelling. Not all the methods have the same purpose; some focus on risk or privacy concerns, while some are more customer-focused.
**STRIDE, DREAD, and PASTA** are among the common threat modelling methodologies.
## **STRIDE**  

STRIDE stands for Spoofing, Tampering, Repudiation, Information Disclosure, Denial Of Service, and Elevation/Escalation of Privilege. STRIDE is a widely used threat model developed by Microsoft which evaluates the system's design in a more detailed view. We can use STRIDE to identify threats, including the property violated by the threat and definition.
1. **Spoofing:** It is an act of impersonation of a user by a malicious actor which violates the authentication principle from the perspective of the CIA triad. Common ways include ARP, IP, and DNS spoofing.
    
2. **Tampering:** The modification of information by an unauthorised user. It violates the integrity principle of the CIA triad.
    
3. **Repudiation:** Not taking responsibility for events where the actions are not attributed to the attacker. It violates the principle of non-repudiability. For example, the attacker clears up all the logs that could lead to leaving traces.
    
4. **Information Disclosure:** It is an act of violation of confidentiality of the CIA triad. A typical example is data breaches.
    
5. **Denial of Service:** Denial of Service occurs when an authorised user cannot access the service, assets, or system due to the exhaustion of network resources. DoS is a violation of the availability principle of the CIA triad.
    
6. **Elevation/Escalation of Privilege:** Escalating privileges to gain unauthorised access is a classic example of a violation of the authorisation principle of the CIA triad.
## **DREAD**

The abbreviation DREAD stands for five questions about each potential: Damage Potential, Reproducibility, Exploitability, Affected Users and Discoverability. DREAD is also a methodology created by Microsoft which can be an add-on to the STRIDE model. It's a model that ranks threats by assigning identified threats according to their severity and priority. In other words, it creates a rating system that is scored based on risk probability. Without STRIDE, the DREAD model also can be used in assessing, analysing and finding the risk probability by threat rating.
1. **Damage:** refers to the possible damage a threat could cause to the existing infrastructure or assets. It is based on a scale of 0–10. A score of 0 means no harm, 5 means Information Disclosure, 8 means user data is compromised, 9 means internal or administrative data is compromised, and 10 means unavailability of a service.
    
2. **Reproducibility:** it measures the complexity of the attack. So how easily a hacker can replicate a threat. A score of 0 means it is nearly impossible to copy, 5 stands for being complex but possible, 7.5 for an authenticated user and a score of 10 means the attacker can reproduce very quickly without any authentication.
    
3. **Exploitability:** Referring to the attack's sophistication or how easy it would be to launch the attack. A score of 2.5 implies it would require an advanced skill set of networking and programming skills; 5 means can be exploited with available tools, a score of 9 means we would need a simple web application proxy tool and a score of 10 means it can exploit through a web browser.
    
4. **Affected Users:** it describes the number of users affected by the successful exploitation of a vulnerability. A score of 0 would mean that there would be no affected users, 2.5 shall mean for an individual user, 6 would mean a small group of users, 9 would mean significant users like administrative users, and 10 would imply all users are affected.
    
5. **Discoverability:** The process of discovering the vulnerable points in the system. For example, the threat would be easily found in case of compromise. A score of 0 would mean it would be challenging to discover it, a score of 5 means that the threat can be discovered by analysis of HTTP requests, and 8 means it can be easily found as it's public-facing. A score of 10 would mean it's visible in the browser address bar.
## Pasta

PASTA is short for Process for Attack Simulation and Threat Analysis; it is a risk-centric threat modelling framework. PASTA's focus is to align technical requirements with business objectives. PASTA involves the threat modelling process from analysing threats to finding ways to mitigate them, but on a more strategic level and from an attacker's perspective. It identifies the threat, enumerates them, and then assigns them a score.
![[Pasted image 20240908132435.png]]
1. **Define Objectives:** The first stage focuses on noting the structure and defining objectives. This makes the end goal a whole lot clearer and ensures the relevant assets are threat modelled by defining an asset scope.
    
2. **Define Technical Scope:** This is where architectural diagrams are defined, both logical and physical infrastructure. Helpful in mapping the attack surface and dependencies from the environment.
    
3. **Decomposition & Analysis:** Each asset will have a defined trust boundary that encompasses all its components and data in this stage. For example, mapping threat vectors for a payment service and evaluating which components underlying the service can be leveraged for an attack; components can be libraries, dependencies, modules or underlying services etc.
    
4. **Threat Analysis:** This refers to the extracted information obtained from threat intelligence. Useful to identify which applications are vulnerable to specific vectors; for example, a customer/public-facing application can be susceptible to DDOS, unauthorised data alteration etc.
    
5. **Vulnerabilities & Weaknesses Analysis:** it analyses the vulnerabilities of web application security controls. It identifies security flaws in the application and enumerates vulnerabilities. It is highly recommended to add mitigation to the identified threat in this stage. For example, when describing a past incident involving an exploit of a mail server, lessons learned or mitigation: lack of thorough testing before implementation and hardening the server.
    
6. **Attack/Exploit Enumeration & Modelling:** In this stage, we map out the possible threat landscape and the entire attack surface of our web application. We then map all potential attack vectors to the different nodes, identifying exploits and attack paths. This stage simulates all the enumerated information extracted from all of the previous steps; this helps security professionals determine the extent and probability of successfully launching the identified vulnerabilities.
    
7. **Risk Impact Analysis:** Based on the collective data from the previous stages, all of the scoped assets that have been affected are analysed and finally, based upon the risk analysis, recommended steps to mitigate the risks and eliminate all of the residual risks are documented.