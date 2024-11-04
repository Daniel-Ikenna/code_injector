## Code Injector

A Python script that intercepts HTTP responses and injects custom JavaScript code into HTML pages.

### Features

- Intercepts HTTP responses on a target network
- Injects JavaScript code into HTML responses for customization or testing

### Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Daniel-Ikenna/code_injector
   ```

2. **Configure the JavaScript Injection**:
   Replace `injection_code` in the script with your desired JavaScript code or URL.

3. **Set Up iptables**:
   Add an iptables rule to direct packets to the netfilter queue:
   ```bash
   sudo iptables -I FORWARD -j NFQUEUE --queue-num 0
   ```

4. **Run the Script**:
   ```bash
   sudo python code_injector.py
   ```

5. **Reset iptables**:
   After use, clear the iptables rule:
   ```bash
   sudo iptables --flush
   ```

### Requirements

- Python 3.x
- `scapy` and `netfilterqueue` libraries (install via `pip install scapy netfilterqueue`)
- Superuser privileges (use `sudo`)

### Important Note

This script is intended strictly for educational and testing purposes. Unauthorized use on networks is prohibited.

### Authors

- [Zaid Sabih](https://ie.linkedin.com/in/zaid-sabih-al-quraishi-5444a6127)
- [Uzoeshi Daniel](https://www.linkedin.com/in/daniel-ikenna-33b709235)
