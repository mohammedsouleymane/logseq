- **Authentication security** is a foundational element of computer security, serving as the proof of an asserted identity. While **identification** is simply the act of stating who a user is, **authentication** is the process of verifying that claim to ensure only authorized entities can take specific actions.
- ### Key Concepts in Authentication Security
- **Controlled Access:** This is the basis of traditional computer security, where people, processes, or devices are authorized to perform actions on specific assets.
- **Multifactor Authentication (MFA):** Security is significantly enhanced by requiring multiple "factors," such as **something you know** (password), **something you have** (physical key/token), or **something you are** (biometrics).
- **Hashing and Salting:** To protect stored credentials, systems use **one-way hashing** (irreversible transformation) rather than reversible encryption. **Salting**—adding unique, non-secret information to a password before hashing—is a critical defense against **rainbow table** attacks.
- **Single Sign-On (SSO):** A mechanism allowing a user to authenticate once to access multiple services, reducing **password fatigue** and administrative overhead, though it creates a **single point of failure**.
- **One-Time Passwords (OTP) and Tokenization:** OTPs provide passwords that expire immediately after one use, while tokenization replaces primary credentials with unique, restricted-scope tokens to avoid repetitive exposure of a master password.
- **Biometrics:** Using physical characteristics like fingerprints, retinas, or voice. While convenient and difficult to forge, they are not impossible to compromise and matches are rarely exact.
- ### Vulnerabilities
  
  A **vulnerability** is a weakness or flaw in a system's software, hardware, or processes that a threat actor can exploit.
- **Causes:** These often arise from **poor coding practices**, design flaws, configuration errors, or even untrained personnel.
- **Zero-Day Vulnerability:** This is a flaw for which **no countermeasure is yet available** because it is unknown to the developer or was discovered by an attacker before a patch could be distributed.
- **Examples of Common Vulnerabilities:** System misconfigurations, **weak or default passwords**, unpatched software, and **broken access control** (where a system fails to verify if a user is authorized for a specific action).
- ### Security Attacks
  
  An **attack** is a deliberate action intended to damage or abuse assets by exploiting a vulnerability.
- #### Password and Physical Attacks
- **Social Engineering:** Manipulating humans into voluntarily revealing secrets. This includes **phishing** (email), **smishing** (SMS), and **vishing** (voice calls). **Spear-phishing** uses personalization to target specific individuals.
- **Guessing Attacks:** **Brute-force attacks** systematically try every possible combination, while **dictionary attacks** use a predefined list of likely passwords.
- **Side-Channel Attacks:** Gaining access by analyzing physical implementation patterns, such as **thermal attacks** on keypads, **smudge attacks** on touchscreens, or analyzing electromagnetic (EM) signals.
- **Supply Chain Attack:** An indirect attack where an adversary compromises a **trusted component** (like a third-party library) in the software development process to infect downstream users.
- #### Major Case Studies
- **Stuxnet (±2010):** Known as the "first digital weapon," it used **four zero-day exploits** to target industrial PLCs and undermine Iran's nuclear program.
- **Heartbleed (2014):** A **buffer overread** vulnerability in the OpenSSL library that allowed attackers to steal private keys and session cookies from 17% of certified domains.
- **Log4Shell (2021):** A **remote code execution** vulnerability in the widely used Log4j logging library, allowing attackers to gain full control of servers through malicious Java Class files.
- **The DAO Exploit (2016):** A **reentrancy vulnerability** in an Ethereum smart contract that allowed an attacker to create a recursive loop and withdraw approximately EUR 50 million in funds.
  
  <!--EndFragment-->
- # Lecture 2
	- ### Assets
	  
	  In computer security, **assets are defined as items of value** that require protection. These are categorized into three main types:
		- **Hardware:** Tangible items such as computer memory, printers, disks, and network gear.
		- **Software:** Intangible assets including operating systems, commercial applications, and cloud services.
		- **Data:** Intangible but often irreplaceable information such as documents, emails, and credentials.
		  
		  Assets can be **tangible or intangible**, and their value is context-dependent. Because assets are often **interconnected and interdependent**, a security breach in one can impact many others.
	- ### CIA+ Properties
	  
	  The **CIA triad** represents the three core pillars of computer security:
		- **Confidentiality:** Ensuring that assets are accessed only by authorized parties. Key mechanisms include **authentication** (verifying identity), **authorization** (enforcing access rights), and **encryption**.
		- **Integrity:** Guarding assets against unauthorized or improper modification. It is maintained through properties like **hashing** (one-way cryptographic functions) and **digital signatures**.
		- **Availability:** Ensuring authorized users have timely and reliable access to assets upon demand. This is supported by **redundancy**, **backups**, and **fault tolerance**.
		  
		  The **CIA+ model** extends these concepts to include properties like **accuracy** (keeping info free from error), **authenticity** (assuring information is genuine), **possession** (independent control of info), and **utility** (the value of info for a specific purpose).
	- ### Security Approaches
	  
	  High-level philosophies guide the design of security policies:
		- **Zero Trust:** A model based on the principle of **"never trust, always verify,"** where no person or device is trusted by default, even inside a network perimeter. It requires continuous authentication and authorization.
		- **Defense in Depth:** A holistic approach that uses **multiple layers of defense mechanisms** (Physical, Network, Host, Data, and Application layers). If one layer is compromised, others remain to provide a barrier.
		- **The Defender’s Dilemma:** A core challenge where the **attacker only needs to succeed once**, while the **defender must be constantly vigilant** and get everything right all the time.
		  
		  <!--EndFragment-->
	- ### Threats and Attacks
	  
	  Understanding security requires distinguishing between weaknesses and the actions taken against them:
		- **Vulnerability:** A bug, flaw, or weakness in a system's software, hardware, or processes that can be exploited. Examples include **system misconfigurations**, weak/default passwords, or unpatched software.
		- **Threat:** Any circumstance or event with the potential to damage or abuse assets. Threats are categorized by the **STRIDE model**, which identifies **Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, and Elevation of Privilege**.
		- **Attack:** A **deliberate action** intended to exploit a vulnerability to harm assets. Examples include **malware**, **phishing**, **spoofing** (impersonation), and **wiretapping** (unauthorized interception).
		- **Denial of Service (DoS):** An attack that renders an asset unavailable to intended users, which can be **volumetric, protocol-based, or even physical** (like cutting cables).
- ### Modeling Security
  
  To rigorously define a security problem, practitioners use models consisting of three ingredients:
	- **System Model:** A description of the assets and their potential vulnerabilities.
	- **Threat Model:** An assessment of the intentions and power of potential attackers (e.g., the attacker can listen on a channel but lacks physical access).
	- **Security Policy:** The specific properties of the system that must be preserved.
	  
	  Examples include **Communications Security models** (focusing on message confidentiality/integrity) and **Access Control models** (such as the Unix multi-user file system permission model).
- ### Security Policies and Mechanisms
  
  Security is attained through a structured approach of rules and enforcement:
	- **Security Policy:** A specification of what is and is not allowed in a system to protect assets, often expressed in terms of CIA+.
	- **Security Mechanism:** The method used to **enforce a security policy**. For example, if a policy requires secrecy, the mechanism might be the use of **encryption**.
	- **Countermeasures (Controls):** Measures used to detect, fix, or prevent risks, ranging from security software and audits to **awareness training**.
	- **Mechanism Types:** These can **prevent, deter, deflect, mitigate, detect, or recover** from an attack.