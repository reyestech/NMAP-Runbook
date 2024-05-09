
<img src="https://i.imgur.com/3cnmaEu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

## NMAP | Runbook

<h2>Hector M. Reyes  | SOC Analyst </h2>
</h1> Group 17: Script K™</h1>
<h1> NMAP: Scanning is an ART </h1>

 ### [Alternative Link | Google Docs | NMAP Runbook](https://docs.google.com/document/d/e/2PACX-1vTemK9_PhnSCm1t8OFJdnwBazk3Qu-vFYuyQzL8kMIGuWRmmnMAOO7PeK4xsDEDs2Hn-lhxUjx_WcON/pub)


<h2>Description</h2>
Nmap, "Network Mapper," is a robust network exploration and security auditing tool. It is an open-source software initially created by Gordon Lyon, known by his pseudonym "Fyodor Vaskovich." The tool is currently maintained and developed by a community of contributors. Nmap can be used on different platforms, including Linux, Windows, and macOS.
<img src="https://i.imgur.com/fSmgUTl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br /> 

Network Mapping
Network mapping identifies and illustrates a computer network's components, connections, and structures. It involves data collection, analysis, and visualization to create a comprehensive network map. By creating a network map, we can understand how devices are interconnected within a network, which is crucial for effective network management, troubleshooting, and security measures. 

Port Scanning <br /> 
One of Nmap's core functionalities. It scans a target host for open, closed, and filtered ports. This information is critical for comprehending network architecture and identifying potential vulnerabilities.
- <b > Identifying open, closed, and filtered ports on a target host. 
- <b > Techniques include TCP SYN scan, TCP connect scan, UDP scan, etc. 
- <b > Users can customize scan parameters such as speed and intensity. 

Service Version Detection  <br /> 
Nmap can identify the version of services running on open ports, which is useful for security auditing and detecting known vulnerabilities that could be exploited.
- <b > Determining the version of services running on open ports. 
- <b > Helps in security assessment and vulnerability detection. 
- <b > Based on specific probes and analyzing responses. 

<img src="https://i.imgur.com/cHllP7u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br /> 

Operating System Detection  <br /> 
Nmap can identify the operating system running on a target host by analyzing various characteristics observed during the scanning process. This feature is helpful for network administrators to determine the types of devices present on the network and for security analysts to assess potential risks associated with specific operating systems.
- <b > Guessing the operating system of a target host. 
- <b > Techniques include TCP/IP stack behavior analysis and network fingerprinting.
- <b > Useful for inventory management and risk assessment.

Scripting Engine  <br /> 
Nmap is a widely used security tool with a powerful scripting engine called NSE (Nmap Scripting Engine). This engine allows users to create and execute custom scripts to automate various tasks during the scanning process. Using NSE, users can efficiently perform advanced functions like vulnerability detection, service enumeration, and more. Nmap's scripting engine is highly flexible and versatile, making it an essential tool for security professionals and enthusiasts.
- <b > Automating tasks during scanning with custom scripts. 
- <b > Scripts perform various functions, such as vulnerability detection and service enumeration. 
- <b > Enhances flexibility and customization of scans. 

Stealthy Scanning Techniques:  <br /> 
Different techniques are available to conduct stealth scans, such as timing control, fragmentation, and decoy hosts. These methods help avoid intrusion detection/prevention systems and maintain a low profile during reconnaissance activities.
- <b > Conducting scans stealthily to evade detection. 
- <b > Techniques include timing control, packet fragmentation, and decoy hosts. 
- <b > It helps avoid triggering intrusion detection/prevention systems (IDS/IPS). 
<br /> <br />

<img src="https://i.imgur.com/jL20w7T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br /> 

Output Formats:  <br /> 
Nmap supports multiple output formats to display scan results, such as plain text, XML, and grepable formats. This flexibility allows users to analyze scan results in various environments and integrate them with other tools and systems.
- <b > Presenting scan results in various formats. 
- <b > Includes plain text, XML, and grepable formats. 
- <b > Allows for easy analysis and integration with other tools.

Extensibility  <br /> 
Nmap's architecture is designed to be extensible, allowing third-party developers to create plugins, scripts, and additional features to enhance its functionality.
- <b > Nmap's architecture allows for creating plugins and scripts. 
- <b > Enhances functionality and customization. 
- <b > Contributes to a rich ecosystem of community-contributed scripts and plugins. 

Legal and Ethical Considerations <br /> 
Nmap is a valuable tool network administrators, security professionals, and researchers use. However, it's crucial to understand that utilizing Nmap for network scanning of networks that are not owned by you or do not have explicit permission for scanning is unethical and illegal. This unauthorized network scanning can lead to privacy violations, computer intrusion, and illicit access laws. Therefore, using Nmap responsibly while staying within the boundaries of applicable laws and regulations is essential.
Purpose  <br /> 
- <b > Network discovery 
- <b > Port scanning 
- <b > Service version detection 
- <b > Operating system detection 
- <b > Vulnerability scanning

<img src="https://i.imgur.com/L6BB7Pq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />   <br /> 

Installation  <br /> 
- <b > Nmap is available for various operating systems, including Linux, Windows, and macOS.
- <b > Installation methods may vary depending on the operating system. 
- <b > You can install Linux using your package manager (apt install nmap for Debian/Ubuntu). 

Basic Usage <br /> 
- <b > Syntax: nmap [Scan Type(s)] [Options] {target specification} 
- <b > Target specification can be a hostname, CIDR notation, or a range of IP addresses. 

Examples:  <br /> 
- <b > Scan a single host: Nmap 192.168.1.1 
- <b > Scan multiple hosts: Nmap 192.168.1.1 192.168.1.2 
- <b > Scan a range of IPs: Nmap 192.168.1.1-100 
- <b > Scan an entire subnet: Nmap 192.168.1.0/24 

Common Scan Types:  <br /> 
- <b > -sS (TCP SYN Scan): Stealthy scan sends SYN packets to determine open ports. 
- <b > -sT (TCP Connect Scan): Completes the TCP handshake to establish a connection. 
- <b > -sU (UDP Scan): Scans UDP ports for open services. 
- <b > -sV (Version Detection): Attempts to determine service versions. 
- <b > -O (OS Detection): Attempts to identify the operating system. 
- <b > -A (Aggressive Scan): Enables OS detection, version detection, script scanning, and traceroute. 

Additional Options <br /> 
- <b > -p (Port Specification): Specify ports or port ranges to scan. 
- <b > -T (Timing Template): Adjust scan timing (0-5, higher is faster but less reliable). 
- <b > -oA (Output to All Formats): Save scan results in all formats (Nmap, XML, and grepable). --script (Script Scanning): Run specific Nmap scripts for additional information gathering or vulnerability detection.

Example Usage <br /> 
- <b > Scan a target with default options: Nmap 192.168.1.1

<img src="https://i.imgur.com/7ZYosQ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br /> 

- <b > Perform an SYN scan with OS detection: nmap -sS -O 192.168.1.1

<img src="https://i.imgur.com/LFr3tyy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br /> 

- <b > Scan specific ports: nmap -p 80,443 192.168.1.1

<img src="https://i.imgur.com/i6Xipxg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br /> 

- <b > Save results to a file: nmap -oA scan_results 192.168.1.1 

<img src="https://i.imgur.com/j5ZXvPk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br /> 

Tips:  <br /> 
- <b > Use caution when scanning networks you don't own or haven't been authorized to scan. 
- <b > Refer to the Nmap documentation and community resources for advanced usage and best practices. 
- <b > Regularly update Nmap and its scripts to benefit from the latest features and vulnerability checks. 

<img src="https://i.imgur.com/7PIr3ZT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<br /> <br /> 

Conclusion <br /> 
Nmap is a powerful network scanning tool for various purposes, including network inventory, security auditing, and vulnerability assessment. Understanding its features allows you to effectively utilize Nmap to gather valuable information about target networks and systems. 
- <b > This runbook provides a basic overview of Nmap and its usage. Refer to the Nmap documentation and online resources for more detailed information and advanced usage.
<br /> <br />

<img src="https://i.imgur.com/fsHfr6b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

