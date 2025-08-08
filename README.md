#  Task 4: Setup and Use a Firewall on Windows

 Objective
Configure Windows Firewall to block and allow specific network ports, then document the changes.

# Steps Followed
1. Blocked Port 23 (Telnet)
- Opened `wf.msc` (Windows Firewall with Advanced Security)
- Created a new **Inbound Rule**:
  - Rule Type: Port
  - Protocol: TCP
  - Port: 23
  - Action: Block the connection
  - Applied to: Domain, Private, Public
  - Rule Name: `Block Telnet Port 23`

2. Allowed Port 22 (SSH)
- Created another inbound rule:
  - Port: 22
  - Action: Allow
  - Rule Name: `Allow SSH Port 22`

3. Removed Block Rule
- Deleted the `Block Telnet Port 23` rule to restore original settings.


##  Interview Questions & Answers

1. What is a firewall?
A firewall is a system that monitors and controls incoming and outgoing network traffic based on predefined security rules.

 2. Difference between stateful and stateless firewalls?
- **Stateful**: Remembers connection states and tracks ongoing traffic.
- **Stateless**: Evaluates packets independently without memory of prior traffic.

 3. What are inbound and outbound rules?
- **Inbound rules** control traffic coming *into* your device.
- **Outbound rules** control traffic *leaving* your device.

 4. How does UFW simplify firewall management?
UFW provides a simplified CLI for managing iptables on Linux, using readable commands like `ufw allow 80`.

 5. Why block port 23 (Telnet)?
Port 23 is used for Telnet, which is insecure and transmits data unencrypted — making it a target for attackers.

6. What are common firewall mistakes?
- Accidentally blocking essential ports like SSH or HTTP
- Misconfigured profiles (e.g., only Public selected)
- Not reviewing or testing rules after applying

7. How does a firewall improve network security?
By restricting access, a firewall prevents unauthorized entry, controls traffic, and protects against malicious attacks.

8. What is NAT in firewalls?
**NAT (Network Address Translation)** allows multiple devices to share a single public IP while keeping internal IPs hidden from external users — improving security and reducing IP usage.

9. Files in This Repo
- `firewall_config.txt`: Simulated firewall configuration steps
-  `README.md`: Documentation and interview question responses
Screenshots couldn’t be included due to system limitations. All steps were documented based on actual Windows Firewall usage.
