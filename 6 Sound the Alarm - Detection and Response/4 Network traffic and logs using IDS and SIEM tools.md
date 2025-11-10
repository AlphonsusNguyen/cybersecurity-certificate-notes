## Logs

Types:

- Network: Proxies, firewalls, etc
- System: OS
- Application: Specific programs
- Security: Security tools like IDS / IPS
- Authentication logs: Login attempts

CSV, JSON, XML, Syslog are some examples
Syslog entry includes three sections: a header, structured-data, and a message
## Detection systems

- HIDS: Host-based IDS, installed on a host / endpoint.
- NIDS: Network-based IDS, installed on network tech, monitors all traffic going through.

### Techniques

- Signature analysis: A signature is a pattern that is associated with malicious activity. Low false positives, easy to evade, require updates and can't deal with unknown. 
- Anomaly-based analysis: In detection phase, the current system activity is compared against this baseline in training phase. Can detect new threats, has high rate of false positives. Pre-existing compromise (attacker existed in training phase).

### Signatures

Signatures specify detection rule, typically contain 3 things:

- Action: Alert / pass / reject (usually)
- Header: Src / dst IP address / ports / protocols
- Rule options: Additional options, e.g. filtering out noisy service

Signature analysis is a detection method used to find events of interest using patterns
## Suricata

IDS, IPS, and NSM (network security monitoring).
Example of a Suricata signature/rule: Action, Header, Rule Options.
Rules processed in a different default order: pass, drop, reject, and alert.
Rules can be customized.

Log files:

- `eve.json`: Standard log file, in JSON format.
- `fast.log`: Basic logging, shouldn't really be used.

Notes: Telemetry refers to the collection, transmission, and measurement of data.
## Some SIEM Tools
SIEM tools process raw data so that it is formatted consistently.
# Google SecOps (Chronicle) [Google Security Operations quickstart guide](https://cloud.google.com/chronicle/docs/review-security-alert)
Use Unified Data Model (UDM)
# Splunk [Splunk’s Search Manual](https://docs.splunk.com/Documentation/Splunk/9.0.1/Search/GetstartedwithSearch)
Use Search Processing Language (SPL)
