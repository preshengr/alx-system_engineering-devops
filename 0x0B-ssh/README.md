# 0X0B-ssh

This directory contains files related to SSH configuration and management. These files are licensed to ALX Holberton School.

## Files:

1. **0-use_a_private_key**: Instructions or script for using a private SSH key.
2. **1-create_ssh_key_pair**: Instructions or script for creating an SSH key pair.
3. **100-puppet_ssh_config.pp**: Puppet manifest for SSH configuration.
4. **2-ssh_config**: SSH configuration file.
5. **school**: Private SSH key.
6. **school.pub**: Public SSH key.

## Authors:

- Presh Engr

## How to Use:

Follow these steps to utilize the files in this directory:

1. **Using a Private Key (`0-use_a_private_key`)**:
   - Follow the instructions provided in the file `0-use_a_private_key` to learn how to use a private SSH key.

2. **Creating an SSH Key Pair (`1-create_ssh_key_pair`)**:
   - Follow the instructions provided in the file `1-create_ssh_key_pair` to generate an SSH key pair.

3. **Configuring SSH with Puppet (`100-puppet_ssh_config.pp`)**:
   - If you're using Puppet for configuration management, apply the Puppet manifest `100-puppet_ssh_config.pp` to configure SSH according to your needs.

4. **SSH Configuration (`2-ssh_config`)**:
   - Use the file `2-ssh_config` as your SSH configuration file. You can place it in the appropriate location on your system (`~/.ssh/config` for user-specific configurations or `/etc/ssh/ssh_config` for system-wide configurations) and customize it as necessary.

5. **SSH Keys (`school` and `school.pub`)**:
   - Use the files `school` (private key) and `school.pub` (public key) as your SSH key pair. Ensure proper permissions are set for the private key (`600` recommended).

By following these steps, you can effectively utilize the provided files for SSH configuration and management in your environment.