# 0x12-web_stack_debugging_2

## Description

This directory contains scripts and configurations aimed at debugging and managing a web stack. The tasks include switching user identities, running Nginx as a non-root user, and applying a quick fix for a common issue in seven lines or less. Each file provides a targeted solution to enhance the security and functionality of your web stack.

## Directory Contents

1. **0-iamsomeoneelse**
2. **1-run_nginx_as_nginx**
3. **100-fix_in_7_lines_or_less**

## File Details and Usage Instructions

### 0-iamsomeoneelse

**Description:**
This script changes the identity of the current user to another user, similar to the `su` (substitute user) command. It allows you to execute commands as another user without logging out and logging back in.

**Usage Instructions:**

1. **Open the File:**
   - Open the `0-iamsomeoneelse` file in a text editor to review the script.

2. **Ensure Proper Permissions:**
   - Ensure the script has execute permissions. You can set the permissions using:
     ```sh
     chmod +x 0-iamsomeoneelse
     ```

3. **Run the Script:**
   - Execute the script, passing the username of the user you want to switch to as an argument:
     ```sh
     ./0-iamsomeoneelse <username>
     ```
   - Replace `<username>` with the actual username you wish to switch to.

4. **Verify the User Switch:**
   - After running the script, check the current user to confirm the switch:
     ```sh
     whoami
     ```

### 1-run_nginx_as_nginx

**Description:**
This script or configuration file ensures that the Nginx web server runs as the `nginx` user, enhancing security by avoiding running the server as a root user.

**Usage Instructions:**

1. **Open the File:**
   - Open the `1-run_nginx_as_nginx` file in a text editor to review the configuration changes.

2. **Modify Nginx Configuration:**
   - Edit the Nginx configuration file, typically located at `/etc/nginx/nginx.conf`, to ensure Nginx runs as the `nginx` user. Add or modify the following line:
     ```sh
     user nginx;
     ```

3. **Ensure Nginx User Exists:**
   - Verify that the `nginx` user exists on your system. If not, create it:
     ```sh
     sudo useradd -r nginx
     ```

4. **Apply Configuration:**
   - Save the configuration file and restart Nginx to apply the changes:
     ```sh
     sudo systemctl restart nginx
     ```

5. **Verify the User:**
   - Check the running Nginx processes to ensure they are running as the `nginx` user:
     ```sh
     ps aux | grep nginx
     ```

### 100-fix_in_7_lines_or_less

**Description:**
This file contains a script that addresses a common system issue with a concise solution in seven lines or less. The specific issue and solution will vary, but the goal is to provide a quick and efficient fix.

**Usage Instructions:**

1. **Open the File:**
   - Open the `100-fix_in_7_lines_or_less` file in a text editor to review the script and understand the issue it addresses.

2. **Ensure Proper Permissions:**
   - Ensure the script has execute permissions. You can set the permissions using:
     ```sh
     chmod +x 100-fix_in_7_lines_or_less
     ```

3. **Run the Script:**
   - Execute the script to apply the fix:
     ```sh
     ./100-fix_in_7_lines_or_less
     ```

4. **Verify the Fix:**
   - After running the script, verify that the issue has been resolved. The verification steps will depend on the specific issue addressed by the script.

## Conclusion

This directory provides essential scripts and configurations for debugging and managing a web stack. Follow the detailed usage instructions to implement and verify each task effectively, ensuring your web stack is secure, functional, and running smoothly.
