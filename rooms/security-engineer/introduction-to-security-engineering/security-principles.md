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

  ‣ Confidentiality ensures only authorized people can access data.  
  ‣ Integrity ensures data cannot be altered and changes can be detected.  
  ‣ Availability ensures systems and services are accessible when needed.  

  For example, in online shopping, confidentiality protects credit card details, integrity prevents altered shipping addresses, and availability ensures the website or app remains accessible. Depending on context, one element may matter more, such as a university announcement where integrity is more important than confidentiality.

  Beyond CIA, two more key aspects are:
  
  ‣ Authenticity means verifying that data or documents are genuine and from the claimed source.  
  ‣ Nonrepudiation means ensuring the sender cannot deny their actions or authorship, which is essential for areas like banking or large transactions.

  Parkerian Hexad expands security to six elements: Availability, Utility, Integrity, Authenticity, Confidentiality, and Possession.

  The two remaining elements are:
  
  ‣ Utility, focuses on keeping information useful, for example when encrypted data becomes inaccessible without a decryption key.  
  ‣ Possession, refers to protecting data from unauthorized access, copying, or control, such as when an attacker steals a backup drive or encrypts data with ransomware.  

- DAD
  

- Fundamental Concepts of Security Models  
   

- Defence-in-Depth

  
- ISO/IEC 19249


- Zero Thrust Versus Trust but Verify
    

- Trust Versus Risk

  Security engineers must balance security with business needs, considering factors like operations, cost, implementation, and usability. While complete isolation is the most secure state, it prevents achieving business goals. Therefore, a security engineer’s decisions must align security measures with organizational objectives.  

  <img src="./screenshots/Screenshot%20(4494).png" alt="Nmap Recon Example" width="500"><br>
  <img src="./screenshots/Screenshot%20(4495).png" alt="Nmap Recon Example" width="500"><br>
  <img src="./screenshots/Screenshot%20(4496).png" alt="Nmap Recon Example" width="500"><br>
  <img src="./screenshots/Screenshot%20(4497).png" alt="Nmap Recon Example" width="500"><br>
  <img src="./screenshots/Screenshot%20(4498).png" alt="Nmap Recon Example" width="500">

- Conclusion

  A security engineer is responsible for an organization’s cybersecurity, ensuring systems and infrastructure are built securely, maintaining and improving the security posture over time, and supporting other teams to achieve a collectively secure environment.
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

