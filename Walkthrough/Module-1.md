# Incident handling #

An **event** is an action occurring in a system or network. Example: Sending Email  
An **incident** is an event with a negative consequence. Example: System Crash, Unauthorized Access

![Module Logo](https://cdn.services-k8s.prod.aws.htb.systems/content/modules/logo/9e65e8b5-217b-46e7-b8bc-eb0a305dd2f4.png)

<span style="color:#58a6ff"> ***Incident handling*** is a clearly defined set of procedures for managing and responding to security incidents in a computer or network environment. </span>

### Different Types of Real-World Incidents ###
- Leaked Credentials 
    - Colonial Pipeline Ransomware Attack  
- Default / Weak Credentials
    - Mirai Botnet (2016)
    - LogicMonitor Incident (2023)
- Outdated Software / Unpatched Systems
    - Equifax (2017) Breach
    - WannaCry (2017)
- Rogue Employee / Insider Threat
    - Cash App / Block Inc. (2021 Disclosure; Public 2022 Notice)
- Phishing / Social Engineering
    - U.S. Interior Department Phishing Attack
    - 2020 Twitter Account Hijacking
- Supply-Chain Attack
    - SolarWinds Orion (2020)
 


## Cyber Kill Chain ##
![cykill](https://cdn.services-k8s.prod.aws.htb.systems/content/modules/148/Cyber_kill_chain.png)
This shows seven stage of attack. Before respond to an incident, it is important to know how an incident (attack) is actually happening. 

The first stage is `recon` where an attacker gather intel about the company or organization.
![recon](https://cdn.services-k8s.prod.aws.htb.systems/content/modules/148/ir_recon.png)

The second stage is <mark>Weaponize</mark> where an attacker builds a stealthy piece of malware (avoids AV/EDR) and packages it into a payload. The information gained from <mark>recon</mark> process is used here to build the payload.

In the third stage, `Delivery`, the attacker gets the payload in front of the victim. The **most common method** is phishing. A malicious email attachment or a link to a web page is very common. Attackers also use **phone-based social engineering**, calling the victim and convincing them to run a payload. And when digital delivery isn't an option, attackers fall back on **physical delivery**.

The fourth stage is `exploitation`: this stage comes when the delivered payload is triggered. Now, the attacker usually execute codes to gain access or control

The fifth stage `Installation`'s goal is simple: make the malware persistent on the compromised machine.
A few `installation` techniques:
- **Dropers:** A small piece of code designed to install malware on the system and execute it
- **Backdoor:** A backdoor is a type of malware designed to provide the attacker with ongoing access to the compromised system
- **Rootkits:** A rootkit is a type of malware designed to hide its presence on a compromised system. Rootkits can be installed through `Droppers`.

In the `Command and Control` stage, the attacker establishes a <mark>remote</mark> access capability to the compromised machine.

The final stage of the chain is the `Action` or `objective` of the attack


##MITRE ATT&CK Framework##
Another framework for understanding adversary behavior is the MITRE ATT&CK framework. It is a more granular, matrix-based knowledge base of adversary tactics and techniques used to achieve specific goals.
![MTIRE](https://cdn.services-k8s.prod.aws.htb.systems/content/modules/148/mitreintro.png)

####Tactic####
- A high-level adversary objective during an intrusion. Examples:
      -Initial Access.
      -Persistence.
      -Privilege Escalation     

