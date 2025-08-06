# Diamond Model of Intrusion Analysis – Lesson Summary and Application

## Overview
This write-up documents my completion and reflection on the "Diamond Model" lesson from TryHackMe. The Diamond Model provides a structured approach for analyzing cyber intrusions, focusing on relationships between the adversary, their capabilities, infrastructure, and the victim. I used this model to analyze the 2015 Ukraine power grid attack in conjunction with the E-ISAC & SANS ICS Report.

## The Diamond Model – Core Features

| Core Feature    | Description |
|----------------|-------------|
| **Adversary**   | The attacker(s) responsible for the intrusion. Can be broken down into adversary operators (who execute the attacks) and adversary customers (who benefit from them). |
| **Victim**      | The target of the attack, including persona (e.g., roles, organizations) and assets (e.g., IPs, domains, systems). |
| **Capability**  | Tools, techniques, and procedures (TTPs) used to conduct the attack, including malware, exploits, and skills. |
| **Infrastructure** | Hardware, software, or services used to deliver capabilities or maintain control. Can be adversary-owned or intermediary-based. |

## Application: Ukraine Power Grid Attack (2015)
Using the Diamond Model, I broke down the Ukraine cyberattack as follows:

### Adversary
- **Operator**: Likely Sandworm Team (APT group)
- **Customer**: Potentially Russian state-sponsored interests seeking geopolitical disruption
- **TTPs**: Spearphishing, BlackEnergy 3 malware, KillDisk wiper, SSH access

### Victim
- **Persona**: Ukrainian regional power companies and their IT/ICS staff
- **Assets**: ICS systems (e.g., SCADA), VPN gateways, operator credentials, substation breakers

### Capability
- **Initial Access**: Phishing with malicious Excel macros
- **Malware**: BlackEnergy (backdoor), KillDisk (wiper)
- **Lateral Movement**: Stolen credentials and RDP/SSH usage
- **Impact**: ICS compromise, power outage affecting approximately 225,000 people

### Infrastructure
- **Type 1**: C2 servers used for remote control
- **Type 2**: Compromised email servers and VPNs for stealth and staging

## Additional Meta-Features

| Feature       | Application in Ukraine Case |
|---------------|-----------------------------|
| **Timestamp** | December 23, 2015, 3:30pm (local outage time) |
| **Phase**     | All phases of the Cyber Kill Chain were present |
| **Result**    | Success – major grid outage, integrity and availability compromised |
| **Direction** | Adversary-to-Infrastructure → Infrastructure-to-Victim |
| **Methodology** | Spearphishing, lateral movement, ICS sabotage |
| **Resources** | Custom malware, C2 infrastructure, stolen credentials, remote access |

## What I Learned
- Developed practical threat intelligence analysis skills using a recognized framework.
- Learned to distinguish adversary roles, infrastructure types, and victim profiles.
- Gained experience applying structured analysis to real-world attacks.
- Strengthened understanding of how malware campaigns interface with critical infrastructure.

> ![Screenshot of THM Flag from Practice Analysis](image1.jpg)
