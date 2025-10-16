# Section 2 — Security Principles

**🔗 Link:** [TryHackMe — Security Principles](https://tryhackme.com/room/securityprinciples)

---

### 🧠 What this section covers
> Learn about the security triad and common security models and principles.

---

### 📘 Content
- Introduction  
  Perfect security doesn’t exist, so the goal is to strengthen defenses by understanding adversaries and applying suitable controls.  
  This section will:
  
  ‣ Explain the CIA triad (Confidentiality, Integrity, Availability).  
  ‣ Present its opposite, DAD (Disclosure, Alteration, Destruction/Denial).  
  ‣ Introduce security models like Bell-LaPadula.  
  ‣ Explain principles such as Defence-in-Depth, Zero Trust, and Trust but Verify.  
  ‣ Introduce ISO/IEC 19249.  
  ‣ Clarify the differences between Vulnerability, Threat, and Risk.
  
- CIA  
  To evaluate security, we use the CIA triad:

  ‣ Confidentiality, ensures only authorized people can access data.  
  ‣ Integrity, ensures data cannot be altered and changes can be detected.  
  ‣ Availability, ensures systems and services are accessible when needed.  

  For example, in online shopping, confidentiality protects credit card details, integrity prevents altered shipping addresses, and availability ensures the website or app remains accessible. Depending on context, one element may matter more, such as a university announcement where integrity is more important than confidentiality.

  Beyond CIA, two more key aspects are:
  
  ‣ Authenticity, means verifying that data or documents are genuine and from the claimed source.  
  ‣ Nonrepudiation, means ensuring the sender cannot deny their actions or authorship, which is essential for areas like banking or large transactions.

  Parkerian Hexad expands security to six elements: Availability, Utility, Integrity, Authenticity, Confidentiality, and Possession.

  The two remaining elements are:
  
  ‣ Utility, focuses on keeping information useful, for example when encrypted data becomes inaccessible without a decryption key.  
  ‣ Possession, refers to protecting data from unauthorized access, copying, or control, such as when an attacker steals a backup drive or encrypts data with ransomware.  

- DAD

  A system’s security can be compromised through disclosure, alteration, or destruction of data.

  Disclosure is the opposite of confidentiality, such as when medical records are stolen and published online.
  Alteration is the opposite of integrity, like when patient records are modified, leading to harmful consequences.
  Destruction or denial is the opposite of availability, as seen when a hospital’s digital systems become inaccessible, halting operations.

  These three form the DAD triad, the opposite of the CIA triad. Protecting against disclosure, alteration, and destruction is essential to maintaining confidentiality, integrity, and availability. However, focusing too much on one can weaken the others, so achieving balance among the three is key to good security.

- Fundamental Concepts of Security Models

  Security models are used to build systems that uphold confidentiality, integrity, and availability. Three foundational models are:

  Bell-LaPadula Model focuses on confidentiality through three rules:  
  ‣ Simple Security Property (“no read up”) prevents lower-level subjects from reading higher-level data.  
  ‣ Star Security Property (“no write down”) prevents higher-level subjects from writing to lower-level objects.  
  ‣ Discretionary Security Property uses an access matrix to control read and write operations.  

  These can be summarized as “write up, read down.” The model, however, does not handle file-sharing.  

  Biba Model focuses on integrity through two rules:  
  ‣ Simple Integrity Property (“no read down”) prevents high-integrity subjects from reading lower-integrity data.  
  ‣ Star Integrity Property (“no write up”) prevents low-integrity subjects from writing to higher-integrity objects.  

  This model follows “read up, write down” but does not address insider threats.  

  Clark-Wilson Model also maintains integrity using:  
  ‣ Constrained Data Items (CDIs) whose integrity must be preserved.  
  ‣ Unconstrained Data Items (UDIs) such as external input.  
  ‣ Transformation Procedures (TPs) that maintain CDI integrity.  
  ‣ Integrity Verification Procedures (IVPs) that validate CDIs.  

  Other notable models include Brewer-Nash, Goguen-Meseguer, Sutherland, Graham-Denning, and Harrison-Ruzzo-Ullman.

- Defence-in-Depth

  Defence-in-Depth, also known as Multi-Level Security, involves building multiple layers of protection. For example, securing valuables might include locking the drawer, the room, the apartment door, and the building gate, plus adding security cameras. Each layer adds a barrier that blocks or slows down potential attackers, strengthening overall security.
  
- ISO/IEC 19249

  ISO and IEC developed ISO/IEC 19249:2017, a standard outlining key architectural and design principles for building secure products, systems, and applications. It introduces five architectural principles and five design principles that guide secure system development.

  Architectural Principles:  
  1. Domain Separation: Groups related components into separate domains with specific security attributes, preventing unauthorized access between them.  
  2. Layering: Structures systems in multiple levels (like the OSI model) so that security policies can be applied and validated at different layers.  
  3. Encapsulation: Hides internal details and restricts direct access, ensuring components interact only through defined interfaces or APIs.  
  4. Redundancy: Enhances availability and integrity by duplicating critical components, such as power supplies or storage drives.  
  5. Virtualization: Shares hardware among multiple operating systems, providing isolation and sandboxing to improve security.  

  Design Principles:  
  1. Least Privilege – Grants users and systems only the permissions necessary to perform their tasks.  
  2. Attack Surface Minimization – Reduces potential vulnerabilities by disabling unnecessary services and components.  
  3. Centralized Parameter Validation – Validates all inputs in a centralized manner to prevent exploitation through invalid or malicious data.  
  4. Centralized General Security Services – Manages essential security functions, such as authentication, from a central and controlled point.  
  5. Preparing for Error and Exception Handling – Designs systems to fail safely, avoiding data leaks or insecure behavior during errors or crashes.  
  
  Together, these principles aim to ensure confidentiality, integrity, and availability while promoting resilience and secure system design.

- Zero Thrust Versus Trust but Verify

  Trust plays a vital role in both personal and business contexts, but in cybersecurity, it must be managed carefully. Two key security principles that help guide how trust should be handled are Trust but Verify and Zero Trust.

  Trust but Verify
This principle emphasizes that even when we trust an entity—such as a user, system, or vendor—we should still verify its behavior. Verification often involves setting up proper logging mechanisms and reviewing activity logs to ensure nothing unusual has occurred. Since manually verifying every action is impractical, automated tools such as proxies, intrusion detection systems (IDS), and intrusion prevention systems (IPS) are used to monitor and validate trusted entities.

  Zero Trust
The Zero Trust principle treats trust itself as a potential vulnerability. It operates on the idea of “never trust, always verify.” Every entity, whether a user or device, is considered untrusted until verified. Access is granted only after authentication and authorization, regardless of the entity’s location or ownership. This model contrasts with traditional security approaches that automatically trust internal networks or company-owned devices.

  One common Zero Trust implementation is microsegmentation, where a network is divided into very small segments—sometimes as small as a single host. Each segment requires authentication and access control before communication is allowed.

  While applying Zero Trust extensively may affect business operations, implementing it as much as feasible can significantly limit the impact of potential breaches and improve overall security posture.

- Trust Versus Risk
  In information security, three key terms are:

  Vulnerability, a weakness that can be exploited.  
  Threat, a potential danger that can exploit a vulnerability.  
  Risk, the likelihood that a threat will exploit a vulnerability and the resulting impact on the business.  

  For example, a showroom with glass doors has a vulnerability in the glass, a threat that the glass can be broken, and a risk determined by the chance of breakage and its business impact. Similarly, in a hospital, a database with a known exploit represents a vulnerability and threat, and the risk must be assessed to decide on mitigation steps.

  <img src="./screenshots/Screenshot%20(4494).png" alt="Nmap Recon Example" width="500"><br>
  <img src="./screenshots/Screenshot%20(4495).png" alt="Nmap Recon Example" width="500"><br>
  <img src="./screenshots/Screenshot%20(4496).png" alt="Nmap Recon Example" width="500"><br>
  <img src="./screenshots/Screenshot%20(4497).png" alt="Nmap Recon Example" width="500"><br>
  <img src="./screenshots/Screenshot%20(4498).png" alt="Nmap Recon Example" width="500">

- Conclusion
This room introduced key security concepts and principles. You learned about the CIA and DAD triads, authenticity, nonrepudiation, vulnerability, threat, and risk. Three security models were discussed along with ISO/IEC 19249. Security principles covered include defence in depth, trust but verify, and zero trust. The Shared Responsibility Model was highlighted for cloud security, showing that security depends on both the cloud provider and the user. For instance, IaaS users control the operating system, while SaaS users do not, making clear role-based responsibilities essential.
---

### 📝 Answer Needed  

| Task | Question | Answer |
|------|-----------|--------|
| **Task&nbsp;1** | — | No answer needed |  
| **Task 2** | Who ensures that an organization's cyber security risk is minimized at all times? | Security Engineer |
| **Task 3** | Where are details about an organization's digital assets, such as name, IP address, and owner, stored? | Asset Inventory |
|  | Sometimes security policies can't be followed because of business needs. What avenue does a security engineer have to fulfil business needs in these cases? | Exceptions |
|  | What philosophy, if followed, provides the most Return on Investment (ROI)? | Secure by Design |
| **Task 4** | What is considered the weakest link in an organization's security? | Humans |
|  | An organization's security evolves with the organization. What helps a security engineer keep the organization secure through these changes? | Change Management |
| **Task 5** | What is a theoretical exercise carried out to gauge the operational readiness of an organization from a security point of view? | Tabletop Exercise |
|  | What is the priority of the management in case of a disaster or crisis? | Business Continuity |
| **Task 6** | Finish the task and capture your own flag | `THM{S#######_3########_R##}` |
| **Task 7** | — | No answer needed |

