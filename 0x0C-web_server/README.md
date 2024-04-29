# 0x0C-web_server

This directory contains files related to configuring and managing a web server using Nginx and Puppet.

### Files:

1. **0-transfer_file**
   - **Description:** Script to transfer a file from your client to a server.
   - **Usage:** Run `./0-transfer_file <IP> <username> <path to file>` to transfer a file to the specified server.

2. **1-install_nginx_web_server**
   - **Description:** Script to install Nginx web server.
   - **Usage:** Run `./1-install_nginx_web_server` to install Nginx on your server.

3. **2-setup_a_domain_name**
   - **Description:** Guide to setup a domain name.
   - **Usage:** Follow the instructions in the file to properly configure a domain name for your server.

4. **3-redirection**
   - **Description:** Guide to configure a redirection on your Nginx server.
   - **Usage:** Follow the instructions in the file to set up redirections on your Nginx server.

5. **4-not_found_page_404**
   - **Description:** Guide to configure a custom 404 Not Found page on your Nginx server.
   - **Usage:** Follow the instructions in the file to set up a custom 404 page.

6. **7-puppet_install_nginx_web_server.pp**
   - **Description:** Puppet manifest to install Nginx web server.
   - **Usage:** Apply the manifest using Puppet with `puppet apply 7-puppet_install_nginx_web_server.pp` to install Nginx on your server.

## Authors
Engr Presh

## Licensed to
ALX Holberton School

## Disclaimer
Please ensure you understand and agree to the terms of the license before using any of the files in this directory.