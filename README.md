# Enhanced-IP-Port-Scanner

Here's a README for your Enhanced IP Range Port Scanner:

🚀 Enhanced IP Range Port Scanner
This is a Python-based graphical user interface (GUI) tool for scanning IP address ranges for open ports. It supports specifying a range of IP addresses and multiple ports (either individual or ranges). Additionally, for common web ports (80 and 443), it attempts to retrieve a preview of the HTML content, offering basic service banner identification. All scan results are saved to a CSV file and separate text files for open and closed ports.

✨ Features
IP Range Scanning: Scan a continuous range of IP addresses (e.g., 192.168.1.1 to 192.168.1.255).

Flexible Port Specification:

Scan individual ports (e.g., 80,443,22).

Scan port ranges (e.g., 1-1024).

Combine both (e.g., 20-23,80,443,8080-8088).

Service Banner Grabbing (HTTP/HTTPS): For open ports 80 (HTTP) and 443 (HTTPS), the tool attempts to fetch the first 200 characters of the HTML content, providing an initial look at what's running on that port.

Multi-threading: The scanning process runs in a separate thread to keep the GUI responsive during long scans.

Progress Bar: A visual progress bar indicates the scanning progress.

Real-time Output: Scan results are displayed in a scrollable text area as they are discovered.

Result Export:

scan_results.csv: A detailed CSV file containing IP, Port, Status (open/closed), and any retrieved banner/info.

up_ips.txt: Lists all IP:Port combinations that were found to be open.

down_ips.txt: Lists all IP:Port combinations that were found to be closed.

🛠️ Installation & Setup
Prerequisites:

Python 3.x: Make sure you have Python installed on your system. You can download it from python.org.

requests library: This is used for fetching web content. Install it using pip:

Bash

pip install requests
tkinter: This is usually included with standard Python installations. If you encounter issues on Linux, you might need to install it separately (e.g., sudo apt-get install python3-tk on Debian/Ubuntu).

Save the Code:
Save the provided code into a Python file (e.g., port_scanner.py).

🚀 How to Run
Open a terminal or command prompt.

Navigate to the directory where you saved port_scanner.py.

Run the script using Python:

Bash

python port_scanner.py
🖥️ Usage
Start IP: Enter the beginning IP address of the range you wish to scan (e.g., 192.168.1.1).

End IP: Enter the ending IP address of the range (e.g., 192.168.1.10).

Port(s): Specify the ports to scan. You can use:

Individual ports: 80,443,22

Port ranges: 1-1024

Combined: 20-23,80,443,8080-8088

The default is 80,443.

Start Scan: Click the "Start Scan" button to begin the scanning process.

View Results:

Results will appear in real-time in the text area.

Upon completion, three files will be generated in the same directory as the script:

scan_results.csv

up_ips.txt

down_ips.txt

⚠️ Important Notes
Scanning Speed: The socket.settimeout(0.5) value determines how long the scanner waits for a response from a port. A smaller value makes the scan faster but might miss some open ports on slow networks. A larger value increases accuracy but slows down the scan.

Ethical Hacking & Legality: Only scan IP addresses and networks for which you have explicit permission. Unauthorized scanning can be illegal and unethical. This tool is intended for educational purposes, network administration, and legitimate security assessments.

Resource Usage: Scanning large IP ranges with many ports can consume significant network resources and time.

Firewalls: Target systems with active firewalls might block port scan attempts or report all ports as closed, even if services are running behind the firewall.

requests Library: The requests library is used for simplified HTTP/HTTPS requests and is generally more robust for web content retrieval than raw sockets for those specific protocols. It's a third-party library and needs to be installed separately.
