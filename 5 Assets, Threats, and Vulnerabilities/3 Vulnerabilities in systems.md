## Vulnerability management

1. Identify vulnerabilities
2. Consider potential exploits
3. Prepare defences against threats
4. Evaluate defences

"Zero-day" = zero days to fix it!

## CI/CD process vulnerabilities
- Risks from Third-Party Code: Regularly scan and update your dependencies. Make sure you’re using secure versions of all external components.
- Misconfigured Permissions: Controlling Access. Ensure only authorized individuals can access and change critical pipeline elements.
- Lack of Automated Security Testing:  Integrate automated security testing (SAST and DAST) into your CI/CD pipeline. Without tools like SAST and DAST, you are almost guaranteed to release software full of vulnerabilities that will go undetected until after it's live, leading to significantly higher costs and effort to fix.
- Exposed Secrets:  Use secure vaults or dedicated secrets management tools to store and manage sensitive information. Enforce this practice across your team. Do not hardcode secrets like like API keys, passwords, and tokens.
- Unsecured Build Environments: Use secure containers or virtual machines to minimize the risk of a compromised pipeline. If the servers and systems that run your pipeline are vulnerable, attackers can compromise it.
- 

## Defense in depth

Also known as the "castle approach", or swiss cheese.

1. Perimeter layer: Usernames & passwords, user authentication.
2. Network layer: Firewalls.
3. Endpoint layer: Protecting devices on network.
4. Application layer: Software defenses.
5. Data layer: Asset classification can help.

## Exposure

- Exposure - A mistake that can be exploited by a threat
- Vulnerability - A weakness of a system

CVE list originally created by MITRE in 1999, now sponsored by US. Goes through review process by CNA (CVE numbering authority). Criteria:

1. Independent of other issues.
2. Recognised as a potential security risk.
3. Submitted with supporting evidence.
4. Only affect one codebase.

The NIST National Vulnerabilities databases uses CVSS (common vulnerability scoring system) to determine severity of vulnerability. Scored on 0-10:

- Under 4.0: Does not require immediate attention.
- Over 9.0: Requires immediate addressing.

## Common vulnerabilities
Broken access control
Cryptographic failures
Injection
Insecure design
Security misconfiguration
Vulnerable and outdated components
Identification and authentication failures
Software and data integrity failures
Security logging and monitoring failures
Server-side request forgery

## OSINT

- Information: Raw data / facts.
- Intelligence: Analysis of info to produce knowledge or insights. Derived with:
  1. Analysis
  2. Interpretation
  3. Integration

## Vulnerabilities

Assessment process:

1. Identification: Discover current state.
2. Vulnerability analysis: Each identified vulnerability tested.
3. Risk assessment: Score assigned to vulnerability (risk x likelihood).
4. Remediation: Actually fixing.

## Teams

- Red: Simulate attacks
- Blue: Defence & incident response
- Purple: Both

## Types of testing

- Open-box: Pen tester has same access as dev.
- Closed-box / black-box: Pen tester has same knowledge as outsider.
- Partial knowledge testing / grey-box: Pen tester has some access / info, e.g. CS.

## Types of threat actor

- Competitor
- State actor
- Criminal syndicate
- Insider threats
- Shadow IT (e.g. using personal email to send work comms)

Note: an APT (advanced persistent threat) is when a threat actor has access for a long period of time.

## Types of hacker

- Unauthorised hacker
- Authorised / ethical
- Semiauthorised (e.g. hacktivist)

## Attack vectors

- Direct (physical) access
- Removable media
- Social media platforms
- Email
- Wireless networks
- Cloud services
- Supply chains

### Defending

- Educating users about vulnerabilities
- Applying least privilege
- Using right security controls & tools

## Feedback

The course is very consistent. Every video is high quality, fits into the theme, etc.
