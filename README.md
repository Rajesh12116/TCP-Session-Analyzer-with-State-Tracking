# TCP-Session-Analyzer-with-State-Tracking
This project analyzes a `.pcapng` file to extract TCP session details using the `pyshark` library. It summarizes TCP streams, packet counts, TCP flags, and deduces connection states (like SYN, ACK, FIN, RST) to give insights into session behavior.


## 🚀 Features

- Parses `.pcapng` files
- Groups packets by 5-tuple: Source IP, Source Port, Destination IP, Destination Port, Protocol
- Tracks TCP Flags: SYN, ACK, PSH, FIN, RST
- Deduces TCP state transitions (e.g., SYN, SYN-ACK, ACK, FIN, RST)
- Clean console output with summary per session

## 📦 Requirements

- Python 3.x
- pyshark
- tshark (Wireshark CLI) installed and accessible via environment variables

### Install dependencies

```bash
pip install pyshark

Run the script:
python tcp_session_analyzer.py

Example Output:
➡️ 192.168.1.244:59937 -> 186.233.187.24:443
   Packets: 15
   Flags: SYN, ACK, PSH, FIN...
   States Seen: SYN, ACK, FIN-ACK


