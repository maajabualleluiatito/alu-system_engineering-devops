UFW Configuration Script

This bash script is designed to configure the Uncomplicated Firewall (UFW) on your Linux system to allow specific incoming traffic while denying all other incoming traffic.
Prerequisites

Before running this script, make sure you have the following:

    A Linux system with UFW installed.
    Superuser (sudo) privileges to execute the commands.

Usage

    Clone or download this repository to your local machine.

    Open a terminal and navigate to the directory where the script is located.

    Make the script executable if it's not already:

    chmod +x ufw-configure.sh

    Run the script with sudo:

    sudo ./ufw-configure.sh

    The script will install UFW if not already installed, set default policies to deny incoming and allow outgoing traffic, and allow incoming traffic on ports 22 (SSH), 80 (HTTP), and 443 (HTTPS).

    UFW will be enabled, and you can check the status using the following command:

    sudo ufw status verbose

Configuration

The script also includes some additional rules:

    It redirects incoming traffic on port 8080 to port 80 using NAT.

    It allows essential ICMP (ping) traffic.

    It permits DHCP client communication.

    It allows multicast DNS and UPnP for service discovery.

    It drops invalid packets and logs them.

Please review the script and adapt it to your specific requirements.
Caution

Modifying firewall rules can impact your server's security and accessibility. Ensure that you understand the rules you are configuring and have tested them in a safe environment before applying them to a production server.
License

This script is provided under the MIT License.

