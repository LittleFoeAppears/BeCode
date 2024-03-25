## Access Control List (ACL) 

Two-Day 

### Preparation

1. Download and install VirtualBox: [https://www.virtualbox.org/](https://www.virtualbox.org/)
2. Download Ubuntu Desktop ISO: [https://ubuntu.com/download/desktop](https://ubuntu.com/download/desktop)
3. Download network scanner tools:
    * Nmap
    * Ping and Traceroute (built-in with most operating systems)

### VM Setup

1. Create two VMs in VirtualBox:
    * VM1 (Router): 2GB RAM, Bridged Adapter network mode.
    * VM2 (Client Machine): 1GB RAM, Internal Network adapter mode.
2. Install Ubuntu Desktop on both VMs.
3. Configure Network:
    * VM1 (Router): Install `iptables` package (`sudo apt update && sudo apt install iptables`).
        * Set static IP for VM1 (e.g., 192.168.1.1) and configure NAT gateway for VM2.
        * Refer to online guides for detailed iptables configuration specific to your router and needs.
    * VM2 (Client Machine): Set manual IP configuration using IP and subnet provided by `ip addr` command in VM1.

### ACL Implementation

1. On VM1 (Router):
    * Use `iptables` commands to create ACLs (refer to online documentation and tutorials).
        * Block specific services (e.g., `iptables -A INPUT -p tcp --dport 25 -j DROP`).
        * Restrict inbound traffic based on ports and devices.
        * Create a guest network (optional) with limited access.
2. On VM2 (Client Machine):
    * Test access to various services and websites.
    * Use `ping` and `traceroute` to verify connectivity.
    * Attempt to access restricted resources and observe error messages.

### Analysis and Documentation

1. Document your steps and observations:
    * Capture screenshots of ACL configurations and access attempts.
    * Note down successful and failed connections, identifying blocked services and ports.
2. Discuss the effectiveness of your ACLs:
    * Did they achieve the desired security level?
    * Are there any unintended consequences or loopholes?
    * How can they be improved?

### Further Exploration

* Explore advanced ACL features like time-based and object-based restrictions.
* Discuss alternative security mechanisms like firewalls and access control matrices (ACMs).
* Consider adding encryption and password protection.

## Resources

- [ACLs on Cisco Routers](https://www.youtube.com/watch?v=0gGhuYOh-54&list=PLIFyRwBY_4bRkAk_BkWL3ea6lRvOn8AKs)
- [ACLs with iptables](https://eng.libretexts.org/Bookshelves/Computer_Science/Operating_Systems/Linux_-_The_Penguin_Marches_On_(McClanahan)/12%3A_Linux_Systems_Security/4.13%3A_Access_Control_Lists___iptables) 
