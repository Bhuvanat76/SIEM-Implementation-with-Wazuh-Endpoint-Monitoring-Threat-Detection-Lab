## **🛡️ Wazuh SIEM Home Lab for Threat Detection and Security Monitoring**



#### **Overview**



This project demonstrates the implementation of a Security Information and Event Management (SIEM) system using Wazuh to monitor endpoint activity, detect suspicious behavior, and simulate cyber attack scenarios.



The environment includes a Wazuh server running on Linux and a Windows endpoint agent monitored for security events. Throughout the project, multiple detection rules and threat simulations were performed to validate the system's capability to identify potential security incidents.



**Project Architecture**



Component	                                                                 Description

* Wazuh Manager	                                      Central SIEM server responsible for event analysis and alert generation
* Wazuh Dashboard	                                      Web interface used to visualize alerts and monitor security events
* Wazuh Indexer	                                      Stores and indexes security logs
* Windows Endpoint	                                      Target system monitored by the Wazuh agent
* Sysmon	                                              Provides enhanced process and network monitoring on Windows



#### **Week 1 – Infrastructure \& Agent Deployment**

###### 

###### **Objective**

Set up the SIEM infrastructure and deploy monitoring agents.



**Tasks Completed**



* Installed Wazuh Manager on Ubuntu server
* Configured Wazuh Dashboard
* Installed Wazuh Indexer
* Deployed Wazuh agent on Windows 10
* Installed Sysmon for enhanced Windows event logging
* Connected Windows endpoint to the Wazuh server
* Verified agent communication and log ingestion



###### **Outcome**

The SIEM infrastructure was successfully deployed and the Windows endpoint began sending system and security logs to the Wazuh server.



#### **Week 2 – Detection Rules \& Log Monitoring**

###### 

###### **Objective**

Configure monitoring rules to detect suspicious activity.



**Tasks Completed**



* Configured File Integrity Monitoring (FIM)
* Monitored sensitive directories for file changes
* Enabled Vulnerability Detection module
* Verified security event collection from Windows
* Tested detection by modifying monitored files
* Observed alerts generated in the Wazuh dashboard



###### **Outcome**

The SIEM system successfully detected file changes and generated security alerts in real time.



#### **Week 3 – Active Response Configuration**

###### 

###### **Objective**

Implement automated response actions for detected threats.



**Tasks Completed**



* Configured Active Response rules in Wazuh
* Implemented firewall-based response actions
* Simulated multiple authentication failures
* Triggered brute-force detection alerts
* Monitored response activity using system logs



###### **Outcome**

Wazuh successfully detected suspicious login attempts and initiated automated response actions based on configured rules.



#### **Week 4 – Threat Simulation \& Attack Detection**

###### 

###### **Objective**

Simulate attacker behavior and validate detection capabilities.



###### **Threat Simulations Performed**



**PowerShell Execution**

Simulated suspicious command execution.

* powershell -ExecutionPolicy Bypass -Command "whoami"



**Account Discovery**

Simulated attacker reconnaissance.

* net user



**System Information Discovery**

* systeminfo



**Suspicious File Creation**

* echo malware > C:\\Users\\Public\\malware.exe



###### **Alerts Observed**



The Wazuh SIEM detected multiple suspicious activities including:



* PowerShell execution events
* Account discovery commands
* Suspicious file creation
* Authentication failures



Alerts were visualized through the Wazuh Security Events dashboard with varying severity levels.



##### **Security Monitoring Capabilities Demonstrated**



This project demonstrates the following cybersecurity monitoring capabilities:



* Endpoint log collection
* Security event correlation
* Suspicious process detection
* Brute-force login detection
* File integrity monitoring
* Automated threat response
* Security alert visualization
* Threat simulation and analysis



###### **Technologies Used**

**Tool**	                                                       **Purpose**



Wazuh	                                                    SIEM platform

Ubuntu Server	                                          Wazuh Manager host

Windows 10	                                          Monitored endpoint

Sysmon	                                               Advanced Windows logging

VirtualBox	                                        Virtual lab environment





##### **Conclusion**



This project successfully implemented a functional SIEM monitoring environment using Wazuh. The system was able to collect logs, detect suspicious activities, generate alerts, and simulate attack scenarios.

The final setup demonstrates how SIEM solutions can help security teams monitor endpoints, identify potential threats, and respond to suspicious activity in real time.



###### Future Improvements



* Possible enhancements for this project include:
* Integration with threat intelligence feeds
* Advanced detection rule customization
* Automated incident response playbooks
* Log monitoring across multiple endpoints
