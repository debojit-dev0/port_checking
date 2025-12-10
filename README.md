# Important Question About Port

1. **What is an open port?**

An open port is like a door on your device that’s ready to accept network connections. If a program is listening on that door (like a web server), that port shows up as “open.”

2. **How does Nmap perform a TCP SYN scan?**

Nmap sends a SYN packet to a port — that’s the first step of a TCP handshake.

If the device replies SYN/ACK, the port is open.

If it replies RST, the port is closed.

If nothing comes back, it’s filtered or blocked.

Nmap never finishes the handshake, which makes the scan fast and quiet.

3. **What risks are associated with open ports?**

An open port can expose a service.
If that service has bugs, weak passwords, or is outdated, attackers can use it to break in.
Unused open ports are unnecessary risk.

4. **Explain the difference between TCP and UDP scanning.**

TCP scan: Clear results because TCP has a handshake.

UDP scan: Less reliable because UDP doesn’t send confirmations. Some UDP services reply, many don’t. It’s slower and harder to interpret.

5. **How can open ports be secured?**
Turn off services you don’t need.

Use a firewall to block outside access.

Keep software updated.

Use strong passwords and authentication.

Limit who can connect to the port.

6. **What is a firewall's role regarding ports?**

A firewall decides which ports are allowed and which are blocked.
It acts like a security guard checking which connections can enter or leave your device.

7. **What is a port scan and why do attackers perform it?**

A port scan checks which ports on a device are open.
Attackers scan because it tells them:

What services are running

Where weaknesses might be
It’s basically mapping the target before attacking.

8. **How does Wireshark complement port scanning?**

Wireshark shows the actual packets that Nmap sends and receives.
You can see SYN, SYN/ACK, RST, timeouts, and filters.
It helps you understand how the scan works and troubleshoot network issues.
