# Redline-Incident-Response-Analysis
# Incident Response Investigation Using FireEye Redline

Author: Franklin Araujo  
Course: BFOR 643  
Date: 5/1/26  

## Project Overview

This project demonstrates how FireEye Redline can be used as an incident response and forensic analysis tool to investigate a potentially compromised Windows system. The goal of the project was to collect host-based evidence, review suspicious activity, and identify indicators of compromise that may not be detected by traditional antivirus tools.

The project focuses on using Redline to examine system artifacts such as running processes, memory-related activity, network connections, and IOC results. This reflects a realistic incident response workflow where an analyst must determine whether a host shows signs of compromise.

## Project Relevance

FireEye Redline is important in incident response because it gives analysts deeper visibility into endpoint activity. During an investigation, responders often need to look beyond alerts and examine what is actually happening on the system.

Redline is useful for:

- Reviewing running processes
- Identifying suspicious system behavior
- Examining memory and host artifacts
- Investigating possible indicators of compromise
- Supporting triage during the detection and analysis phase of incident response

This tool is especially relevant because modern attackers may use fileless malware, legitimate Windows tools, or memory-based techniques that are harder to detect with basic security tools.

For a deeper breakdown of Redline’s role in the incident response lifecycle, see:

[Tool Analysis](docs/tool-analysis.md)

## Methodology Summary

The project followed a basic incident response workflow:

1. Set up the Redline analysis environment
2. Collected host-based system data
3. Imported the collection into Redline
4. Reviewed processes and system activity
5. Checked network connections
6. Examined IOC results
7. Documented findings using screenshots and notes

For the full step-by-step process, see:

[Methodology](docs/methodology.md)

## Results

The investigation showed how Redline can help identify suspicious host activity and support incident response decision-making.

Main findings included:

- Suspicious or unusual process activity
- Possible abnormal parent-child process relationships
- Network connection review for external communication
- IOC-based prioritization of suspicious artifacts

## Evidence

### Process Analysis

![Process Analysis](screenshots/process-analysis)

### IOC Detection

![IOC Detection](screenshots/ioc-detection)

### Network Connections

![Network Connections](screenshots/network-connections)

### Memory / Host Artifact Review

![Memory Artifact](screenshots/memory-artifact)

## Results Summary Table

| Area Reviewed | What Was Analyzed | IR Value |
|---|---|---|
| Processes | Running programs and process relationships | Helps detect suspicious execution |
| Memory / Host Artifacts | System-level activity and possible anomalies | Helps identify hidden or fileless behavior |
| Network Connections | Active or unusual connections | Helps determine possible communication with external systems |
| IOC Results | Redline’s flagged indicators | Helps prioritize what should be investigated first |

## Real-World Application

In a real incident response investigation, Redline could be used when a system is suspected of malware infection, unauthorized activity, or abnormal behavior. It allows the analyst to collect and review evidence from the endpoint before deciding whether the system should be isolated, cleaned, or investigated further.

For expanded real-world scenarios, see:

[Real-World Application](docs/real-world-application.md)

## Limitations

Although Redline is useful, it also has limitations:

- It requires analyst interpretation
- It may produce false positives
- It is not a complete replacement for advanced forensic tools
- It is more useful for host-based triage than full enterprise-wide monitoring

## Conclusion

This project showed how FireEye Redline supports incident response by helping analysts investigate endpoint activity, identify possible indicators of compromise, and make informed decisions during an investigation. The main lesson learned is that memory and host-based analysis are important because not every attack leaves obvious files or alerts.

## Repository Structure
redline-incident-response-analysis/
```text

 ┣ README.md
 ┣ docs/
 ┃ ┣ tool-analysis.md
 ┃ ┣ methodology.md
 ┃ ┗ real-world-application.md
 ┣ screenshots/
 ┣ logs/
 ┗ data/
