# NMAP-Runbook

<h1>Hector M. Reyes  | SOC Analysts </h1>
</h1> Group 17: Script K™</h1>
<h1> NMAP Runbook  </h1>

<h2>Description</h2>  <br/> 
Nmap, short for "Network Mapper," is a powerful open-source tool for network exploration and security auditing. It was initially written by Gordon Lyon, commonly known by his pseudonym "Fyodor Vaskovich," and is actively maintained and developed by a community of contributors. Nmap is available for various platforms, including Linux, Windows, and macOS.
<br /><br />
<img src="https://i.imgur.com/lcl7mD5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

  
<br /><br />

Network Mapping <br /> 
Nmap is primarily used for network mapping, which involves discovering hosts and services on a computer network. It allows users to determine what hosts are available on the network, what services (application name and version) those hosts offer, what operating systems (and OS versions) they are running, what type of packet filters/firewalls are in use, and other related information. Discovering hosts and services on a network.

Port Scanning <br /> 
One of Nmap's core functionalities is port scanning. It can scan a target host to identify open, closed, and filtered ports. This information is crucial for understanding the network architecture and potential vulnerabilities. 
- <b > Identifying open, closed, and filtered ports on a target host. 
- <b > Techniques include TCP SYN scan, TCP connect scan, UDP scan, etc. 
- <b > Users can customize scan parameters such as speed and intensity. 

Service Version Detection  <br /> 
Nmap can determine the version of services running on open ports. This is useful for security auditing and determining whether any services are running with known vulnerabilities that could be exploited. 
- <b > Determining the version of services running on open ports. 
- <b > Helps in security assessment and vulnerability detection. 
- <b > Based on specific probes and analyzing responses. 

Operating System Detection  <br /> 
Nmap can guess the operating system of a target host based on various characteristics observed during the scanning process. This feature is helpful for network administrators to identify the types of devices present on the network and for security analysts to assess potential risks associated with specific operating systems. 
- <b > Guessing the operating system of a target host. 
- <b > Techniques include TCP/IP stack behavior analysis and network fingerprinting.
- <b > Useful for inventory management and risk assessment.

Scripting Engine  <br /> 
Nmap includes a scripting engine (NSE - Nmap Scripting Engine) that allows users to write and execute scripts to automate various tasks during the scanning process. These scripts can be used for vulnerability detection, service enumeration, and more. 
- <b > Automating tasks during scanning with custom scripts. 
- <b > Scripts perform various functions, such as vulnerability detection and service enumeration. 
- <b > Enhances flexibility and customization of scans. 

Stealthy Scanning Techniques:  <br /> 
Nmap provides several options for conducting scans stealthily, including options for timing control, fragmentation, and decoy hosts. These techniques help to avoid detection by intrusion detection/prevention systems (IDS/IPS) and maintain a low profile during reconnaissance activities. 
- <b > Conducting scans stealthily to evade detection. 
- <b > Techniques include timing control, packet fragmentation, and decoy hosts. 
- <b > It helps avoid triggering intrusion detection/prevention systems (IDS/IPS). 

Output Formats:  <br /> 
Nmap supports various output formats for presenting scan results, including plain text, XML, and grepable formats. This flexibility enables users to analyze scan results in different environments and integrate them with other tools and systems. 
- <b > Presenting scan results in various formats. 
- <b > Includes plain text, XML, and grepable formats. 
- <b > Allows for easy analysis and integration with other tools.

Extensibility  <br /> 
Nmap's architecture is designed to be extensible, allowing third-party developers to create plugins, scripts, and additional features to enhance its functionality. 
- <b > Nmap's architecture allows for the creation of plugins and scripts. 
- <b > Enhances functionality and customization. 
- <b > Contributes to a rich ecosystem of community-contributed scripts and plugins. 

Legal and Ethical Considerations <br /> 
While Nmap is a valuable tool for network administrators, security professionals, and researchers, it's important to note that using Nmap for unauthorized scanning of networks you don't own or have explicit permission to scan is illegal and unethical. Unauthorized scanning can violate computer intrusion, privacy, and unauthorized access laws. Therefore, using Nmap responsibly and within the bounds of applicable laws and regulations is essential. 

Purpose  <br /> 
- <b > Network discovery 
- <b > Port scanning 
- <b > Service version detection 
- <b > Operating system detection 
- <b > Vulnerability scanning 

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

- <b > Perform an SYN scan with OS detection: nmap -sS -O 192.168.1.1

- <b > Scan specific ports: nmap -p 80,443 192.168.1.1 

- <b > Save results to a file: nmap -oA scan_results 192.168.1.1 



Tips:  <br /> 
- <b > Use caution when scanning networks you don't own or haven't been authorized to scan. 
- <b > Refer to the Nmap documentation and community resources for advanced usage and best practices. 
- <b > Regularly update Nmap and its scripts to benefit from the latest features and vulnerability checks. 

Conclusion <br /> 
Nmap is a powerful network scanning tool for various purposes, including network inventory, security auditing, and vulnerability assessment. Understanding its features allows you to effectively utilize Nmap to gather valuable information about target networks and systems. 
- <b > This runbook provides a basic overview of Nmap and its usage. Refer to the Nmap documentation and online resources for more detailed information and advanced usage.




