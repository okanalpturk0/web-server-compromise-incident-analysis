# Web Server Compromise: Incident Analysis

A cybersecurity incident analysis project investigating a simulated web server compromise involving a brute-force attack, malicious JavaScript injection, and browser redirection.

## Project Overview

This project documents the investigation of a compromised cooking website, `yummyrecipesforme.com`, using a supplied tcpdump traffic log and supporting incident evidence.

The analysis focuses on identifying network protocols, reconstructing the observed connection sequence, documenting the attack, and recommending a security control.

## Objectives

- Identify DNS, TCP, and HTTP activity in tcpdump logs.
- Analyze the observed network connection sequence.
- Document the brute-force attack and malicious code injection described in the scenario.
- Recommend a mitigation for repeated administrative login attempts.
- Distinguish directly observed network evidence from scenario-based findings.

## Tools and Technologies

- tcpdump — network traffic analysis
- DNS — domain name resolution
- TCP — connection establishment
- HTTP — web communication
- Markdown — technical documentation

## Key Findings

- DNS A-record queries resolved both domains to IPv4 addresses in the sample log.
- TCP three-way handshakes established connections to the two websites.
- HTTP GET requests accessed the root webpage of each domain.
- The scenario's source-code and file-analysis findings identified malicious JavaScript injection and redirection behavior.
- The scenario attributed the initial compromise to brute-force password guessing against an administrator account using a default password.

## Recommended Mitigation

Implement login attempt rate limiting to reduce the effectiveness of automated password guessing. Use temporary restrictions, progressive delays, and appropriate monitoring to balance security with legitimate administrative access.

## Repository Structure

- `report/incident-report.md` — detailed incident report
- `evidence/tcpdump-log.txt` — supplied sample traffic log
- `evidence/evidence-analysis.md` — packet-level observations and interpretations
- `docs/attack-flow.md` — attack sequence and protocol overview
- `REFERENCES.md` — learning materials and references

## Scope and Disclaimer

This is a simulated educational incident analysis based on a course scenario and supplied sample traffic. It is not a forensic investigation of a live production system. No live attack was conducted as part of this documentation.

## References

- [GitHub README documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
- Course-provided tcpdump traffic log and incident scenario
