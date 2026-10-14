- **`ipconfig`**
    - Displays basic information for each network adapter, including your **IPv4 Address**, **Subnet Mask**, and **Default Gateway**. Use this to verify that your router has assigned your computer a valid local IP address.
- **`ipconfig /all`**
    - Shows full network details for all adapters. Use this to check your physical **MAC address**, check your **DHCP status** (whether your IP is automatic or static), and find the exact IP addresses of your **DNS Servers** and router.

2. Network Troubleshooting & IP Resets

- **`ipconfig /release`**
    - Drops your current IPv4 address lease from your router's DHCP server. This disconnects you from the network temporarily.
- **`ipconfig /renew`**
    - Requests a fresh IP address assignment from your router's DHCP server. (Commonly used immediately after a `/release` to fix a stuck or glitched local connection).

3. DNS Cache Troubleshooting

- **`ipconfig /flushdns`**
    - Clears your computer's local DNS resolver cache. Run this if a website or local server changed its IP address but your computer is still trying to connect to the old, broken location.
- **`ipconfig /displaydns`**
    - Lists all stored DNS cache records currently saved in your system's memory. Use this to see exactly which domains your computer has recently looked up.
- **`ipconfig /registerdns`**
    - Refreshes all DHCP leases and re-registers your computer's local DNS hostname with the network's DNS server.

4. Help Utility

- **`ipconfig /?`**
    - Displays the official help menu outlining all available ipconfig switches, syntax formats, and parameters.
