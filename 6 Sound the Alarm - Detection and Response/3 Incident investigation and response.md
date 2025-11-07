## Common Indicators of Compromise (IoCs) in CI/CD Pipelines
 - Unauthorized Code Changes:
Code changes from people who shouldn't be making changes.
Code changes made at unusual times or from unexpected locations.
Code changes that look suspicious, like confusing code, very large deletions without a good reason, or code that doesn't follow coding rules.
- Suspicious Deployment Patterns:
Deployments to unusual or unapproved systems (for example, production deployments started directly from developer branches).
Deployments happening at unexpected times or too often (deployments outside of planned release times).
Deployments started by unusual user accounts or automated accounts that shouldn't be releasing to production.

- Compromised Dependencies:
Finding known vulnerabilities (CVEs) in dependencies during automated checks in the CI/CD pipeline.
Suddenly adding new, unexpected dependencies to build settings.
Attempts to download dependencies from unofficial or untrusted sources.
 - Unusual Pipeline Execution:
 - Secrets Exposure Attempts:
Logs showing attempts to get to secrets from unapproved places in the pipeline.
Finding private secrets hardcoded in code changes (ideally prevented earlier, but monitoring can catch mistakes).

## Proactive Security Through Monitoring for IoCs
 - Respond to Incidents Quickly
 - Limit the Damage
 - Improve Threat Knowledge

## Using Automation to Find Anomalies and IoCs
 - Comprehensive Logging and Auditing 
# The most common logs for finding anomalies include:
 - Pipeline Execution Logs
 - Code Commit Logs 
 - Access Logs 
 -Deployment Logs

# Security Information and Event Management (SIEM) Integration
 - Automatically Find Anomalies: SIEMs use machine learning and analytics to automatically find unusual patterns in CI/CD logs, which are  possible IoCs to investigate.
 - Use Rules to Alert for Known IoCs: You can set up specific rules in the SIEM to find known CI/CD IoCs. For example, rules can send alerts when:
-  Detection of specific malicious file hashes (related to known CI/CD attacks) are found in build results.
 - CI/CD servers connect to known malicious command and control (C2) servers (using threat intelligence data).

Real-time Alerting and Notifications for:
 - Unusual Build Failures
 - Suspicious Code Changes (Based on Anomalies)
 - Attempts to Expose Secrets
 - Unusual Network Traffic

Performance Monitoring to Find IoAs and Discover IoCs 
Continuous Vulnerability Scanning

## Indicators

- Indicators of Compromise: Observable evidence that suggests potential security incident. You can think of an IoC as evidence that points to something that's already happened
- Indicators of Attack: Series of events that suggest real time incident.

> Essentially, IoCs help to identify the who and what of an attack after it's taken place, while IoAs focus on finding the why and how of an ongoing or unknown attack. For example, observing a process that makes a network connection is an example of an IoA. The filename of the process and the IP address that the process contacted are examples of the related IoCs.

## Pyramid of pain

Higher on the IoC pyramid = harder for an attacker to work around any blocks.

TTP = Tactics, techniques, and procedures.
https://detect-respond.blogspot.com/2013/03/the-pyramid-of-pain.html

<img width="1600" height="845" alt="image" src="https://github.com/user-attachments/assets/ce09edd5-b4d9-4cfb-b11d-c91b7e77e200" />

## Documentation

3 benefits:

1. Transparency (chain of custody). Transparent documentation is useful as a source of evidence for security insurance claims, regulatory investigations, and legal proceedings. 
2. Standardization (incident response plan)
3. Clarity
Best practices: Know your audience, Be concise and Update regularly.
## Triage

1. Receive and assess
2. Assign priority
3. Collect and analyze

# The containment, eradication, and recovery phase of the lifecycle
Containment is the act of limiting and preventing additional damage caused by an incident.
Eradication involves the complete removal of the incident elements from all affected systems
Recovery is the process of returning affected systems back to normal operations

# BCP
a business continuity plan (BCP) is a document that outlines the procedures to sustain business operations during and after a significant disruption. A BCP helps organizations ensure that critical business functions can resume or can be quickly restored when an incident occurs.

## Post-incident activity
 - A lessons learned meeting
 - Final report (be mindful about the audience you're writing for)
