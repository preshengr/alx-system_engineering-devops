# 0x0A Configuration Management

This directory contains Puppet manifests for configuration management tasks. These manifests are licensed to ALX-Holberton School.

## Files:

1. **0-create_a_file.pp**: Puppet manifest to create a file.
2. **1-install_a_package.pp**: Puppet manifest to install a package.
3. **2-execute_a_command.pp**: Puppet manifest to execute a command.

## How to Use:

Follow these steps to use the provided Puppet manifests:

1. **Install Puppet**: If Puppet is not already installed on your system, you can install it by following the instructions provided on the official Puppet website: [Puppet Installation Guide](https://puppet.com/docs/puppet/latest/installing_and_upgrading.html)

2. **Clone the Repository**: Clone the repository containing the Puppet manifests to your local system.

    ```
    git clone <https://github.com/preshengr/alx-system_engineering-devops.gitl>
    ```

3. **Navigate to the Directory**: Change your current directory to the `0x0A-configuration_management` directory.

    ```
    cd 0x0A-configuration_management
    ```

4. **Execute the Manifests**: To execute any of the provided manifests, use the `puppet apply` command followed by the filename of the manifest.

    ```
    sudo puppet apply 0-create_a_file.pp
    ```

    Replace `0-create_a_file.pp` with the filename of the manifest you want to execute.

5. **Verify the Changes**: After executing the manifest, verify that the desired changes have been applied to the system. Depending on the manifest, this could involve checking for the creation of a file, installation of a package, or execution of a command.

6. **Repeat as Needed**: Repeat the process for any additional manifests you want to apply.

By following these steps, you can effectively use the provided Puppet manifests for configuration management tasks within your environment.