Cybersecurity Incident Report: Network Traffic Analysis

Objective

In this report, we analyze a network traffic issue related to DNS and ICMP. The objective is to understand the problem detected in the DNS and ICMP traffic logs, explain the analysis process, and identify potential causes of the incident. This will help in implementing appropriate measures to prevent similar issues in the future.

Summary of the Problem

The network traffic analysis reveals that the DNS server, which uses UDP port 53 for resolving domain names, is facing an issue. Specifically, the log shows an ICMP error message indicating that UDP port 53 is unreachable. This error suggests that the DNS server is either non-responsive or unable to process requests on port 53. This port is crucial for DNS services, and its unavailability directly impacts the DNS server’s ability to handle requests. The problem is significant as it may hinder the server's functionality, possibly due to an external factor like a Denial of Service (DoS) or Distributed Denial of Service (DDoS) attack.

Analysis of the Data

Time of Incident: 1:24 PM

Initial Detection: The IT team received multiple client reports about webpage access issues. Clients saw an error message indicating "destination port unreachable" when trying to visit the website.

Investigation Process:

Reporting: Analysts reported the issue to their supervisor.
Action Taken: Security engineers began an investigation, including packet sniffing using tcpdump.
Findings: The packet sniffing revealed that DNS port 53 was unreachable. Logs confirmed that the DNS server was not responding.

Cause of Incident: The most likely cause of the incident is a Denial of Service (DoS) attack. This type of attack can overwhelm the DNS server, causing it to be unable to handle legitimate traffic and resulting in the "port unreachable" error observed.

Steps Taken

Verification of Port Status: Through packet sniffing, the team verified that UDP port 53 was indeed unreachable. Check for Firewall Issues: The investigation also considered whether the firewall was blocking traffic to port 53, but the primary issue appeared to be server overload.

Summary

The analysis identified that UDP port 53, used by DNS services, was unreachable, affecting the DNS server's ability to handle requests. The incident likely resulted from a DoS attack designed to overwhelm the server, making it unable to process legitimate queries. The issue was first detected through client complaints and confirmed through network analysis. Immediate steps included verifying port status and investigating potential firewall issues. This analysis highlights the need for robust defenses against DoS attacks and the importance of monitoring and responding to network traffic anomalies promptly.
