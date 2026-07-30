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

The first stage is 'recon' where an attacker gather intel about the company or organization.
![recon](https://cdn.services-k8s.prod.aws.htb.systems/content/modules/148/ir_recon.png)

The second stage is <mark>Weaponize</mark> where an attacker builds a stealthy piece of malware (avoids AV/EDR) and packages it into a payload. The information gained from 'recon' process is used here to build the payload.
