# GhostLogin

GhostLogin is a Bash-based remote reconnaissance framework that leverages SSH access to execute intelligence gathering tasks through a target host.  
It includes anonymity verification, whois lookups, remote port scanning, and structured logging.

---

## Overview

GhostLogin performs reconnaissance by connecting to a remote SSH server and executing controlled commands through it.

Core capabilities include:

- Root privilege validation
- Dependency verification and automatic installation
- Anonymity verification using Nipe
- Remote IP extraction
- Country identification
- Uptime extraction
- Whois lookup
- Remote Nmap scanning
- Structured logging

---

## Capabilities

### Environment Validation
- Root privilege enforcement
- Required tool verification:
  - nmap
  - sshpass
  - whois
  - geoiplookup
  - nipe (auto-install if missing)

### Anonymity Verification
- Public IP detection
- GeoIP country lookup
- Optional activation of Nipe for traffic anonymization
- Spoofed IP confirmation

### Remote Reconnaissance
Using SSH access to a remote host:

- Remote public IP extraction
- Target country lookup
- System uptime retrieval
- Whois lookup execution
- Remote Nmap open-port scan

---

## Installation

Clone the repository:

```bash
git clone https://github.com/mishap2001/GhostLogin.git
cd GhostLogin
```

Install required dependencies:

```bash
sudo apt update
sudo apt install nmap sshpass whois geoip-bin curl git
```

Make the script executable:

```bash
chmod +x GhostLogin.sh
```

---

## Usage

Run as root:

```bash
sudo bash GhostLogin.sh
```

The script will prompt for:

1. Target SSH IP address  
2. Target SSH username  
3. Target SSH password  
4. Target address to scan  

---

## Output

The following files are generated:

```
target_data.txt
target_whois.txt
target_nmap.txt
target_log.txt
```

These contain:

- Extracted IP information  
- Country data  
- Uptime information  
- Whois results  
- Open port scan results  
- Execution timestamps  

---

## Author

Michael Pritsert  
GitHub: https://github.com/mishap2001  
LinkedIn: https://www.linkedin.com/in/michael-pritsert-8168bb38a  
