# FUTURE_CS_02
# Firewall Setup Documentation for Kali Linux Using Uncomplicated Firewall (UFW)
This guide will walk you through the process of installing and configuring a firewall on Kali Linux using the Uncomplicated Firewall (UFW). Follow these steps carefully to ensure a secure environment in your virtual machine.
**1. Open Kali Linux in Virtual Machine**
Start by opening your Kali Linux virtual machine. Once it’s booted up, access the terminal.

**2. Update Package List**
Before installing anything, make sure your package list is up to date. Run the following command in the terminal:

```bash
sudo apt update
```
This will ensure your system is aware of the latest available software packages.

**3. Install UFW (Uncomplicated Firewall)**
Next, install UFW, which is a simple firewall tool that makes it easy to configure rules. In the terminal, type:

```bash
sudo apt install ufw
```
This command installs UFW on your system.

**4. Enable UFW**
Once UFW is installed, enable the firewall by running:

```bash
sudo ufw enable
```
This will activate UFW and start enforcing any rules you configure.

**5. Configure Basic Firewall Rules**
To configure basic firewall rules, we will start by allowing SSH (Secure Shell) connections. This is important for remote access to your Kali machine. Run:

```bash
sudo ufw allow SSH
```
Alternatively, you can specify a port number if you want to allow a service on a different port, like HTTP (port 80):
```bash
sudo ufw allow 80/tcp
```
You can add as many rules as needed by replacing the service name (e.g., SSH) with other service names or port numbers.

**6. Check Firewall Status**
After adding the rules, check the current status of UFW to verify your settings. Use the following command:

```bash
sudo ufw status
```
This will display all the rules that have been applied and their current status.

**7. Blocking a Connection**
If you need to block a specific service or connection, you can use the following command. For example, to block HTTP connections:

```bash
sudo ufw deny http
```
This will deny incoming connections on port 80 (HTTP). You can replace "http" with any other service or port.

**8. Remove a Rule**
If you change your mind and wish to remove a rule, you can delete it with the following command. For example, to remove the rule that allows SSH:

```bash
sudo ufw delete allow ssh
```
This will delete the rule that allows SSH connections.

**9. Reload UFW to Apply Changes**
Once you have configured all the rules to your liking, be sure to reload UFW to save and apply the changes for future sessions:

```bash
sudo ufw reload
```
This command reloads the UFW configuration and ensures that your firewall rules are saved.

# Conclusion
You have now successfully set up and configured a firewall using UFW in Kali Linux. This simple yet effective firewall will help secure your system by controlling incoming and outgoing network traffic. You can always modify the rules later to suit your needs.




