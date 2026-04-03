# Network Port Scanner

A lightweight, multi-threaded TCP port scanner with a minimal **Tkinter GUI**. Enter a target host and port range, then scan for open ports — no command-line flags required.

---

## Features

- **Graphical interface** — simple three-field form (Target, Start Port, End Port)
- **Multi-threaded scanning** — up to 500 concurrent threads for fast results
- **DNS resolution** — accepts both IP addresses and hostnames; resolves before scanning
- **Service identification** — recognises common services (FTP, SSH, HTTP, HTTPS, MySQL, RDP, VNC, and more)
- **Live progress bar** — real-time port count and elapsed timer
- **Stop mid-scan** — cancel any running scan instantly
- **Save results** — export discovered open ports to a `.txt` file

---

## Requirements

| Dependency | Notes |
|---|---|
| Python 3.x | Tested on Python 3.8+ |
| `tkinter` | Included in standard Python distributions |

No third-party packages are required.

---

## Installation

```bash
git clone https://github.com/AbhirajSinghrajpoot/Network_scan.git
cd Network_scan
```

---

## Usage

```bash
python portscanergui.py
```

### Steps

1. **Target** — enter an IP address (e.g. `192.168.1.1`) or a hostname (e.g. `scanme.nmap.org`).
2. **Start Port** — first port to scan (default: `1`).
3. **End Port** — last port to scan (default: `1024`).
4. Click **Start Scan**.
5. Open ports are listed in real time in the *Open Ports* panel.
6. When the scan finishes, click **Save Results** to export the findings.

---

## Supported Services

| Port | Service |
|------|---------|
| 21 | FTP |
| 22 | SSH |
| 23 | Telnet |
| 25 | SMTP |
| 53 | DNS |
| 80 | HTTP |
| 110 | POP3 |
| 143 | IMAP |
| 443 | HTTPS |
| 3306 | MySQL |
| 3389 | RDP |
| 5900 | VNC |
| 8080 | HTTP-Alt |

Ports not in the list are reported as `Unknown`.

---

## Project Structure

```
Network_scan/
└── portscanergui.py   # Main application (GUI + scanner logic)
```

---

## Disclaimer

This tool is intended for **authorized network testing and educational purposes only**. Scanning networks or systems without explicit permission may be illegal. Use responsibly.
