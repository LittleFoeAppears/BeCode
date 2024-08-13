# PfSense 

## Exercise: Installing pfSense and Implementing Network Segmentation in VirtualBox

This exercise guides you through installing pfSense on VirtualBox and configuring three isolated virtual networks for enhanced security.

- Type of Challenge: `Learning` 
- Duration: `1 day`
- Deadline: `dd/mm/yy H:i AM/PM`
- Team challenge : `solo`

**Learning Objectives:**

* Install pfSense on VirtualBox.
* Create three virtual networks using VLANs.
* Configure firewall rules for network segmentation.
* Understand the benefits of network segmentation.

**Prerequisites:**

* VirtualBox installed on your host machine.
* Downloaded pfSense ISO image: [https://www.pfsense.org/download/](https://www.pfsense.org/download/)
* Minimum system requirements for both host machine and pfSense VM: [https://www.pfsense.org/download/](https://www.pfsense.org/download/)

**Network Scenario:**

We will create three virtual networks within VirtualBox using pfSense:

1. **LAN (Green):** Trusted internal network.
2. **Guest (Blue):** Isolated network for guests or untrusted devices.
3. **DMZ (Red):** Public-facing network for exposed services.

**Exercise Steps:**

**1. Install pfSense:**

* Follow the steps outlined in the previous response "Installing pfSense on VirtualBox with DMZ Setup (Markdown Format)" to install pfSense on a VirtualBox VM.
* During installation, select the following interface assignments:
    * WAN (red): Bridged adapter connected to your internet modem.
    * LAN (green): Internal network adapter (created within VirtualBox).
    * DMZ (red): Separate internal network adapter (created within VirtualBox) 

**2. Configure VLANs:**

* In the pfSense web GUI, go to **Interfaces** > **Assignments**.
* Create two new VLAN interfaces:
    * **Guest (Blue):** Tag it with a unique VLAN ID .
    * **DMZ (Red):** Tag it with a different VLAN ID .
* Assign the Guest VLAN interface to the internal network adapter dedicated for guest devices.
* Assign the DMZ VLAN interface to the separate internal network adapter dedicated for the DMZ.

**3. Configure Firewall Rules:**

* Go to **Firewall** > **Rules**.
* Create the following rules:

    * **Deny all traffic:** Block all traffic between any interface by default.
    * **Allow specific traffic:** Create specific rules to allow:
        * LAN to Guest: Only necessary traffic (e.g., web browsing, limited internet access).
        * Guest to LAN: Only allow specific outbound traffic (e.g., DNS lookups).
        * LAN to DMZ (optional): Only necessary traffic for exposed services.
        * DMZ to WAN (optional): Only allowed outbound traffic for the exposed services.
        * WAN to any: Block all incoming traffic by default.

**4. Verify and Test:**

* Connect devices to each virtual network adapter (LAN, Guest, DMZ).
* Verify connectivity within each isolated network.
* Test allowed traffic flow based on your firewall rules.
* Ensure blocked traffic remains inaccessible.

**Additional Notes:**

* This exercise provides a basic setup. You can customize further based on your specific needs.
* Consult the pfSense documentation https://docs.netgate.com/pfsense/en/latest/ for detailed instructions and advanced configurations.
* Remember to apply best practices for secure configurations with strong passwords and regular updates.
* Always research and understand the potential risks before implementing changes to your network.

**Congratulations!** You have successfully installed pfSense on VirtualBox and implemented basic network segmentation with VLANs. This exercise helps you understand the core concepts and benefits of segmentation, laying the groundwork for exploring more advanced configurations in the future.

## Relevant Resources

https://benheater.com/virtualbox-lab-pfsense-firewall/
https://benheater.com/virtualbox-lab-configure-pfsense/