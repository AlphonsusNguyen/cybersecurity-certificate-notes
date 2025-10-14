## Overview

Security hardening: Strengthening a system to reduce its vulnerabilty and attack surface.
Attack surface: All the potential vulnerabilities.

Conducted on:

- Hardware
- OS
- Applications
- Networks
- Databases
- Physical space

Examples are:

- Patches
- Config changes
- Disabling used services
- Reducing permissions

Regular penetration testing also helps

## OS hardening

Regular interval tasks:

- Patch updates
- Backups
- Wiping old hardware
- Removing unused software

One-off:

- Secure encryption
- Strong password policy

### Baseline configuration

> A baseline configuration is a documented set of specifications within a system that is used as a basis for future builds, releases, and updates.

## Virtual machines (VMs) and sandboxes 
- Virtual machines (VMs) are software versions of physical computers, provice an isolated enviroment to prevent malicious code from affecting the rest of the computer or system. A few malicious program can still escape virtualization and access the host machine.
- Using sandbox (testing environment that allows you to execute software or programs separate from your network, could be physical hardware or software or cloud-based) to test patches, bugs, vulnerabilities.
Some malware authors know how to write code to detect if the malware is executed in a VM or sandbox environment. Attackers can program their malware to behave as harmless software when run inside these types of  testing environments.

## Preventing brute force attacks

- Salting & hashing
- MFA / 2FA
- Captcha
- Strong password policies


## Network hardening

 Four devices used to secure a network: firewalls, intrusion detection systems, intrusion prevention systems, and security incident and event management tools
 <img width="978" height="704" alt="image" src="https://github.com/user-attachments/assets/c9669508-e54e-4a87-bfd1-b15eaa8b259b" />

Regular interval tasks:

- Firewall rules maintenance
- Network log analysis
- Patch updates
- Server backups

One-off:

- Port filtering on firewalls
- Network access privileges
- Using isolated subnets for departments / security zones
- Using modern encryption standards

### Hardware

- Intrusion detection system: Monitors traffic, alerts to possible intrusion.
- Intrusion prevention system: Monitors traffic, actively stops the activity.

## Cloud hardening

Considerations:

- Identity access management (IAM): managing digital identities / authorisations.
- Configuration. Misconfigured cloud services are a common source of cloud security issues.
- Attack surface
- Zero-day attacks (usually patched quicker!)
- Visibility & tracking
- Hypervisors
  + Type 1 runs on host computer hardware, usually used by cloud service providers.
  + Type 2 runs on host computer software.
- ata and applications on a cloud network should be kept separate depending on their service category
- Baselining establishes a fixed reference point for cloud environment configurations to compare changes and improve security.
- Cryptography secures data in the cloud through encryption and secure key management, ensuring data integrity and confidentiality.
