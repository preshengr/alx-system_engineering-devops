# 0x18-webstack_monitoring

This directory is part of the `alx-system_engineering-devops` repository and focuses on web stack monitoring. It contains a script for setting up Datadog on a server to monitor various metrics and logs.

## Directory Structure

- `2-setup_datadog`: A script to install and configure Datadog agent on a server.

## Prerequisites

Before running the script, ensure you have the following:

- A Datadog account
- A Datadog API key
- A server with internet access

## File Details

### 2-setup_datadog

#### Description
This script installs the Datadog agent on a server and configures it to start monitoring the system. It requires a Datadog API key, which you can obtain from your Datadog account.

#### Usage
```bash
sudo ./2-setup_datadog <DATADOG_API_KEY>
```

#### Example
```bash
sudo ./2-setup_datadog d1234567890abcdef1234567890abcdef
```

## Step-by-Step Guide

### 1. Create a Datadog Account

1. **Go to [Datadog](https://www.datadoghq.com/)**.
2. **Sign up for an account or log in if you already have one.**
3. **Navigate to the API keys section (Integrations > APIs) and generate a new API key.**

### 2. Prepare the Server

1. **Open a terminal or SSH into your server.**
2. **Ensure the server has internet access and the necessary permissions to install packages.**

### 3. Clone the Repository

1. **Navigate to the directory where you want to clone the repository.**
2. **Run the following command to clone the `alx-system_engineering-devops` repository:**

    ```bash
    git clone https://github.com/<your-username>/alx-system_engineering-devops.git
    ```

3. **Navigate to the `0x18-webstack_monitoring` directory:**

    ```bash
    cd alx-system_engineering-devops/0x18-webstack_monitoring
    ```

### 4. Run the Setup Script

1. **Make the script executable (if not already):**

    ```bash
    chmod +x 2-setup_datadog
    ```

2. **Run the script with your Datadog API key:**

    ```bash
    sudo ./2-setup_datadog <DATADOG_API_KEY>
    ```

    Replace `<DATADOG_API_KEY>` with your actual Datadog API key.

3. **The script will:**
    - Update the package list.
    - Install required dependencies.
    - Set up the Datadog repository.
    - Install the Datadog agent.
    - Configure the agent with your API key.
    - Start the Datadog agent.

### 5. Verify the Installation

1. **Log in to your Datadog account.**
2. **Navigate to the infrastructure list (Infrastructure > Hosts).**
3. **You should see your server listed and metrics being reported.**

## Notes

- The script requires `sudo` permissions to install and configure the Datadog agent.
- Ensure that the server's firewall allows outgoing connections to Datadog's endpoints.
- Modify the script as needed to include additional configuration settings for the Datadog agent.

## Troubleshooting

- **Agent Not Reporting:**
  - Check the agent status by running `sudo datadog-agent status`.
  - Verify the API key in the configuration file (`/etc/datadog-agent/datadog.yaml`).
  - Ensure there are no network issues preventing the agent from reaching Datadog servers.

- **Permissions Issues:**
  - Make sure you are running the script with `sudo` privileges.
  - Check that the user running the script has permissions to install packages and modify system configurations.

## Additional Resources

- [Datadog Documentation](https://docs.datadoghq.com/)
- [Datadog Agent Troubleshooting](https://docs.datadoghq.com/agent/troubleshooting/)

By following this guide, you should be able to set up Datadog monitoring on your server effectively. Adjust the steps as needed to fit your specific environment and requirements.
