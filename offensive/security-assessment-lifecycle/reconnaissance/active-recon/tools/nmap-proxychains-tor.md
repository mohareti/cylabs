# Nmap + Proxychains + Tor

## Network Scanning via TOR Nodes

You can use the following tools to route your network scanning traffic through the TOR network, enhancing anonymity:

1. **ProxyChains:**
   * Install ProxyChains: `sudo apt-get install proxychains` (on Debian/Ubuntu)
   * Edit the `proxychains.conf` file to specify TOR as a proxy server.
   * Run your scanning tool with `proxychains`.
2. **Nmap with ProxyChains:**
   * Use Nmap with ProxyChains: `proxychains nmap -sS -p <ports> <target>`

## Network Scanning via VPS

You can use a VPS as an intermediary for scanning a target network:

1. **Set up a VPS:**
   * Create or purchase a VPS instance from a provider (e.g., AWS, DigitalOcean).
   * Securely connect to the VPS using SSH.
2. **Install Scanning Tools:**
   * Install Nmap, Masscan, or other scanning tools on the VPS.
3. **Conduct Scanning:**
   * Run scanning commands on the VPS, targeting the desired network.
   * You can use tools like Nmap or Masscan on the VPS.

## Network Scanning via VPN

Using a VPN service for network scanning can provide anonymity and security. Here's how to do it:

1. **Subscribe to a VPN Service:**
   * Choose a reputable VPN service and subscribe to it.
2. **Install VPN Client:**
   * Install the VPN client on your scanning machine.
3. **Connect to VPN:**
   * Connect to the VPN service using the client.
4. **Conduct Scanning:**
   * Run scanning commands (e.g., Nmap, Masscan) while connected to the VPN to route your traffic through the VPN server.

Please note that ethical and legal considerations apply when conducting network scanning. Always ensure that you have proper authorization and are in compliance with applicable laws and regulations before scanning any network. Unauthorized scanning can lead to legal consequences.
