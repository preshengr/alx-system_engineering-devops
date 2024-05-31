# 0x13-firewall

## Description

This directory contains configurations and scripts related to managing firewall settings. Specifically, it includes a configuration to block all incoming traffic except specified exceptions and a script for port forwarding. These files are essential for securing a network by controlling traffic flow and allowing specific services through the firewall.

## Directory Contents

1. **0-block_all_incoming_traffic_but**
   - A configuration file that sets up a firewall rule to block all incoming traffic except for specified ports or services. This is crucial for enhancing security by only allowing necessary traffic to access your network.

2. **100-port_forwarding**
   - A script or configuration file that sets up port forwarding rules. Port forwarding is used to redirect traffic from one port to another, often used to allow external access to services hosted behind a firewall.

## File Details and Usage Instructions

### 0-block_all_incoming_traffic_but

**Description:**
This file contains firewall rules to block all incoming traffic, with exceptions for specific ports or services that you want to allow. 

**Usage Instructions:**

1. **Open the File:**
   - Open the `0-block_all_incoming_traffic_but` file in a text editor to review the rules.

2. **Modify Exceptions:**
   - Edit the file to specify which ports or services should be allowed. For example, you might want to allow incoming traffic on port 80 (HTTP) and port 443 (HTTPS).

3. **Apply Firewall Rules:**
   - Use a command-line interface to apply these rules to your firewall. The exact command depends on your firewall software. For example, if you're using `iptables` on Linux, you might use:
     ```sh
     sudo iptables-restore < 0-block_all_incoming_traffic_but
     ```
   - If you are using `ufw` (Uncomplicated Firewall), you would manually add each rule defined in the file using:
     ```sh
     sudo ufw allow 80/tcp
     sudo ufw allow 443/tcp
     sudo ufw enable
     ```

4. **Verify Rules:**
   - Check the active firewall rules to ensure they are correctly applied:
     ```sh
     sudo iptables -L
     ```
   - Or, if using `ufw`:
     ```sh
     sudo ufw status
     ```

### 100-port_forwarding

**Description:**
This file sets up port forwarding rules to redirect traffic from one port to another. This is useful for allowing external access to internal services.

**Usage Instructions:**

1. **Open the File:**
   - Open the `100-port_forwarding` file in a text editor to review the rules.

2. **Edit Forwarding Rules:**
   - Modify the file to specify the source port, destination port, and the destination IP address. For example, forwarding external traffic from port 8080 to an internal server on port 80.

3. **Apply Port Forwarding Rules:**
   - Apply these rules using the appropriate command for your firewall. For example, with `iptables`:
     ```sh
     sudo iptables -t nat -A PREROUTING -p tcp --dport 8080 -j DNAT --to-destination 192.168.1.100:80
     sudo iptables -t nat -A POSTROUTING -j MASQUERADE
     ```
   - If using `ufw`, you might add rules like this:
     ```sh
     sudo ufw route allow proto tcp from any to any port 8080
     ```

4. **Save and Persist Rules:**
   - Ensure that the rules persist across reboots. With `iptables`, you might save the rules using:
     ```sh
     sudo sh -c "iptables-save > /etc/iptables/rules.v4"
     ```
   - With `ufw`, the rules are automatically persistent.

5. **Verify Forwarding:**
   - Check that the port forwarding rules are correctly applied and functioning as expected:
     ```sh
     sudo iptables -t nat -L -n -v
     ```
   - Or, for `ufw`:
     ```sh
     sudo ufw status numbered
     ```

## Conclusion

This directory provides essential files for managing firewall settings, specifically for blocking incoming traffic with exceptions and setting up port forwarding. Follow the detailed usage instructions to configure and verify your firewall settings effectively, ensuring your network is secure and necessary services are accessible.
