<h1>Detecting Live Cyber Attacks with Microsoft Sentinel & Azure Honeypot VM</h1>

<!--### [YouTube Demonstration](link goes here)-->

<h2>Introduction</h2>

In this project, I guide you through setting up Microsoft Sentinel (formerly Azure Sentinel), a cloud-based SIEM (Security Information and Event Management) system. This SIEM has been integrated with a virtual machine designed as a [honeypot](https://www.crowdstrike.com/cybersecurity-101/honeypots-in-cybersecurity-explained/) to attract and log cyber attacks from around the globe. The primary goal is to offer a practical learning experience in cybersecurity defense mechanisms, SIEM utility, and the analysis of attack patterns through real-time data visualization.

<h2>Components Utilized</h2>

- <b>Microsoft Sentinel for SIEM</b>
- <b>Azure Virtual Machines for the honeypot setup</b>
- <b>Log Analytics Workspace with Kusto Query Language (KQL) Queries for log ingestion</b>
- <b>PowerShell for enhancing log data with geographic information</b>

<h2>Architecture Before Configuration</h2>
The setup begins with creating a vulnerable virtual machine in Sentinel to serve as a honeypot, intentionally exposed to the internet to attract attacks. This VM's logs, particularly failed RDP login attempts, are then ingested into Azure Log Analytics Workspace.
<br/><br/>

- <b>Honeypot VM Setup:</b> Configured to be highly vulnerable, with external and Windows firewalls turned off (proceed with caution!) to simulate an enticing target for attackers.
- <b>Microsoft Sentinel Configuration:</b> Set up to ingest logs from the honeypot VM and visualize attack data.

<h2>Configuration Steps and Management</h2>

- <b>Creating Azure Subscription and VM:</b> Starting with a new Azure subscription and setting up a honeypot VM.
<p align="center">
Azure portal showing the new VM: <br/><br />
<img src="https://res.cloudinary.com/antofon/image/upload/v1707619254/Microsoft%20Sentinel%20SIEM%20with%20Honeypot%20VM%20Lab/Screenshot_2024-02-10_at_6.40.47_PM.png" height="80%" width="80%" alt="Azure portal showing the new VM"/>
<br />
<br />
</p>

- <b>Log Analytics Workspace Setup:</b> Configuring a workspace to ingest logs from the VM.
<p align="center">
Connecting Microsoft Sentinel to Log Analytics Workspace: <br/><br />
<img src="https://res.cloudinary.com/antofon/image/upload/v1707626545/Microsoft%20Sentinel%20SIEM%20with%20Honeypot%20VM%20Lab/Screenshot_2024-02-10_at_8.41.16_PM.png" height="80%" width="80%" alt="Connecting Microsoft Sentinel to Log Analytics Workspace"/>
<br />
<br />
 <img src="https://res.cloudinary.com/antofon/image/upload/v1707626546/Microsoft%20Sentinel%20SIEM%20with%20Honeypot%20VM%20Lab/Screenshot_2024-02-10_at_8.41.51_PM.png" height="80%" width="80%" alt="Connecting Microsoft Sentinel to Log Analytics Workspace"/>
<br />
<br />
 <img src="https://res.cloudinary.com/antofon/image/upload/v1707621196/Microsoft%20Sentinel%20SIEM%20with%20Honeypot%20VM%20Lab/Screenshot_2024-02-10_at_7.04.12_PM.png" height="40%" width="40%" alt="Connecting Microsoft Sentinel to Log Analytics Workspace"/>
<br />
<br />
</p>

- <b>Microsoft Sentinel Integration:</b> Connecting Microsoft Sentinel to the workspace to analyze and visualize the data.

<p align="center">
Connecting Microsoft Sentinel to Log Analytics Workspace: <br/><br />
<img src="https://res.cloudinary.com/antofon/image/upload/v1707621231/Microsoft%20Sentinel%20SIEM%20with%20Honeypot%20VM%20Lab/Screenshot_2024-02-10_at_7.09.08_PM.png" height="75%" width="75%" alt="Connecting Microsoft Sentinel to Log Analytics Workspace"/>
<br />
<br />
 <img src="https://res.cloudinary.com/antofon/image/upload/v1707626277/Microsoft%20Sentinel%20SIEM%20with%20Honeypot%20VM%20Lab/Screenshot_2024-02-10_at_8.37.34_PM.png" height="80%" width="80%" alt="Connecting Microsoft Sentinel to Log Analytics Workspace"/>
</p>

- <b>PowerShell Scripting for Geographic Data:</b> Utilizing PowerShell to extract IP addresses from failed login attempts, enriching this data with geographic information through an external API, and logging this enriched data for visualization.

<!--[screenshot: Enriched log data]-->
- <b>Visualizing Attacks:</b> Using Microsoft Sentinel to create maps and dashboards that display the origin of cyber attacks in real-time.

<p align="center">
Microsoft Sentinel attack map:<br/><br/>
<img src="https://res.cloudinary.com/antofon/image/upload/v1707624917/Microsoft%20Sentinel%20SIEM%20with%20Honeypot%20VM%20Lab/Screenshot_2024-02-10_at_8.14.57_PM.png" height="100%" width="100%" alt="Microsoft Sentinel attack map"/>
</p>

<h2>Security Hardening Measures</h2>

<p>As I develop this project, I would aim to strengthen its security and data analysis capabilities with several enhancements:

- <b>Isolate the Honeypot VM:</b> Implement tighter network segmentation to further isolate the honeypot, minimizing risk to my network.
- <b>Update Firewall Rules:</b> Introduce dynamic firewall rules based on the latest threat intelligence to proactively block emerging threats.
- <b>Expand Monitoring:</b> Utilize Microsoft Sentinel more extensively with custom queries for deeper insight into subtle attack patterns.
- <b>Selective Patching:</b> Strategically update the honeypot to protect against non-critical vulnerabilities while maintaining its intended vulnerabilities.
- <b>Enhance Administrative Security:</b> Strengthen administrative access with multi-factor authentication to prevent unauthorized access.
- <b>Improve Data Protection:</b> Explore encryption techniques to protect collected data, ensuring it remains secure.
- <b>Ensure Legal and Ethical Compliance:</b> Review and adhere to legal and ethical standards in cybersecurity to ensure the project's integrity.</p>

<h2>Key Metrics</h2>
<p>The project's effectiveness was gauged by the ability to capture, enrich, and visualize attack data. Key metrics include:</p>

- <b>Deployment Success:</b> Successful setup of the honeypot VM and integration with Microsoft Sentinel.
- <b>Log Data Enrichment:</b> Successful extraction and enrichment of IP addresses with geographic data using PowerShell.
- <b>Attack Visualization:</b> Effective use of Microsoft Sentinel to create visual representations of cyber attacks, showcasing their global distribution.
- <b>Client Machine Integration:</b> The Windows 10 VM was successfully joined to the domain and could log in using domain credentials.

<h2>Conclusion</h2>
This project showcases the setup and utilization of Microsoft Sentinel as a powerful tool for real-time cybersecurity monitoring and defense. By integrating a honeypot VM with Microsoft Sentinel, I demonstrate a hands-on approach to understanding cyber threats and the importance of SIEM systems in modern cybersecurity practices. This experience is crucial for anyone looking to advance their skills in cybersecurity analysis and defense strategies.
<br />

<!--
```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
