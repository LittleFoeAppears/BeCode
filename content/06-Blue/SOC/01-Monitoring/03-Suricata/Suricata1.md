
## Suricata


- Type of Challenge: Forencics
- Duration: 1 day
- Challenge type : Solo

## Objective

Configure and deploy Suricata in a test environment, analyze network traffic, create custom rules, and generate detailed reports based on your findings.


### Tasks

1. **Environment Setup**

- Install Suricata on a virtual machine.
-Ensure the system has all necessary dependencies installed (e.g., libpcap, libnet, etc.).
- Update the system and Suricata to the latest stable versions.

2. **Initial Configuration**

- Configure the Suricata YAML file (/etc/suricata/suricata.yaml).
- Set up network interfaces for live traffic capture.
- Configure logging to output to both JSON and EVE (for later analysis).

3. **Basic Testing**

- Start Suricata in live mode and ensure it is capturing traffic.
- Generate some network traffic and verify it is being logged by Suricata.
- Use tools like curl, ping, and nmap to generate various types of traffic.

4. **Understanding Suricata Rules**

- Study the existing Suricata rules and understand their structure.
- Read the Suricata documentation on writing custom rules.

5. **Creating Custom Rules**

- Create at least 5 custom Suricata rules that detect specific types of network behavior (e.g., detecting SSH login attempts, HTTP requests to a specific URI, suspicious DNS queries).
- Test these rules by generating the appropriate network traffic and ensure they trigger correctly.

6. **Deliverables**

- A screenshot of the Suricata configuration file.
- Zip file with Logs showing Suricata successfully capturing and logging traffic.
- A brief report (3 pages) on setup, initial findings, issues encountered.