## Homelab : Enterprise NOC Monitoring & Incident Response

## Tools Used
Monitoring: Zabbix 7.0.22
OS/Env: Ubuntu Linux 22.04 (WSL2)
Web Stack: Nginx, PHP 8.3, MariaDB
Testing: Linux stress utility

## Objective
To architect a professional Network Operations Center (NOC) environment capable of real-time health monitoring, high-sensitivity performance alerting, and proactive incident visualization.

## Lab Components
Zabbix Server: Centralized monitoring engine collecting 3.10+ values per second.
Zabbix Agent: Deployed on the target host to monitor 166 internal items and 76 triggers.
NOC Map: A functional "Digital Twin" of the infrastructure for visual triage.

## Configuration Performed
Full-Stack Deployment: Managed service dependencies and verified "active (running)" status of the monitoring daemon.
Logic Tuning: Re-engineered standard CPU triggers from 5-minute averages to instant 1-second thresholds (>20% utilization) to detect stealth spikes.
Visual Mapping: Configured the "SANDEEP-NOC-CORE" map with live-linked host elements for immediate visual status updates.

## Issues Simulated
Service Blackout: Manually terminated the agent to test the availability detection loop.
Resource Exhaustion: Generated a synthetic CPU load that peaked at 38.48% utilization to validate custom trigger sensitivity.

## Troubleshooting & Resolution
Triage: Performed Root Cause Analysis (RCA) via terminal, identifying the service as "inactive (dead)".
Recovery: Executed systemctl start to restore monitoring services.
Verification: Observed the "Global View" dashboard return to a healthy "1 Available" state.

## NOC & Security Relevance
Incident Lifecycle: Mastered the end-to-end process of Detection, Acknowledgment, and Resolution.
Performance Engineering: Applied precision monitoring techniques to reduce "Alert Fatigue" and catch anomalies instantly.
Capacity Planning: Analyzed eth0 network traffic patterns (968 bps peak) to monitor for potential data exfiltration or DDoS signatures.

## Evidence
