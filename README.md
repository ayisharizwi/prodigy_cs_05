Here's a sample README file for your network packet sniffing code:

---

# Network Packet Sniffer

This repository contains a Python script that captures and displays network packets in real time. The script leverages the Scapy library to sniff network traffic, extracting and printing relevant information such as source and destination IP addresses, protocol type, and payload data.

## Features

- **Real-Time Packet Capture**: Sniffs network packets in real-time on a specified interface.
- **Protocol Identification**: Detects and labels common protocols such as TCP, UDP, and ICMP.
- **Payload Extraction**: Displays the payload of TCP and UDP packets if available.

## Installation

To run this script, you need to have Python installed along with the following package:

- [Scapy](https://scapy.net/) (A powerful Python library for network packet manipulation)

You can install Scapy using pip:

```bash
pip install scapy
```

> **Note:** Running this script may require administrative or root privileges to access network interfaces.

## Usage

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/ayisharizwi/prodigy_cs_05.git
   cd prodigy_cs_05
   ```

2. **Run the Script:**

   ```bash
   sudo python packet_sniffer.py
   ```

3. **Network Interface:**

   By default, the script will sniff all IP traffic on the default network interface. You can modify the script to specify a different interface if needed (e.g., `eth0`, `wlan0`).

4. **Example Output:**

   When the script runs, you will see output similar to the following:

   ```
   Source IP: 192.168.1.2 -> Destination IP: 192.168.1.3 | Protocol: TCP
   Payload: b'GET / HTTP/1.1\r\nHost: example.com\r\n\r\n'

   Source IP: 192.168.1.4 -> Destination IP: 192.168.1.5 | Protocol: UDP
   Payload: b'\x1f\x8b\x08\x00\x00\x00\x00\x00\x00\x03'
   ```

## How It Works

1. **Packet Capture:**
   - The script uses the `sniff` function from Scapy to capture packets.
   - It applies a filter to capture only IP packets.

2. **Packet Analysis:**
   - For each packet, the source and destination IP addresses are extracted.
   - The protocol is identified and labeled (TCP, UDP, ICMP, or Other).
   - If the packet contains TCP or UDP payload data, it is displayed in the output.

## Customization

- **Filtering**: You can modify the filter parameter in the `sniff` function to capture specific types of traffic (e.g., "tcp", "udp", "icmp").
- **Interface**: To specify a particular interface, add `iface="your_interface"` to the `sniff` function call.
- **Packet Storage**: Currently, the script does not store packets. You can set `store=1` in the `sniff` function to keep captured packets in memory.

## Contributing

Contributions are welcome! Feel free to submit pull requests or open issues if you have suggestions or encounter problems.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

You can modify this README as needed to suit your repository and any additional features you might add.
