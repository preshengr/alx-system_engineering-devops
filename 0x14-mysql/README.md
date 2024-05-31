# 0x14-mysql

## Description

This directory contains configurations and scripts for setting up and managing MySQL databases, including primary-replica replication and backups. The files provide a comprehensive guide to configuring a primary database, setting up a replica, and performing backups.

## Directory Contents

1. **4-mysql_configuration_primary**
2. **4-mysql_configuration_replica**
3. **5-mysql_backup**
4. **install_log**
5. **replication**
6. **setup.sql**
7. **setup_master**
8. **setup_slave**

## File Details and Usage Instructions

### 4-mysql_configuration_primary

**Description:**
This file contains the MySQL configuration for the primary (master) database server. It includes settings necessary for enabling replication and optimizing performance.

**Usage Instructions:**

1. **Open the File:**
   - Open the `4-mysql_configuration_primary` file in a text editor to review the configuration.

2. **Apply Configuration:**
   - Copy the configuration settings into your primary MySQL server's configuration file, typically located at `/etc/mysql/mysql.conf.d/mysqld.cnf` or `/etc/my.cnf`.

3. **Restart MySQL Service:**
   - Restart the MySQL service to apply the changes:
     ```sh
     sudo systemctl restart mysql
     ```

4. **Verify Configuration:**
   - Check the MySQL logs and status to ensure the configuration is correctly applied:
     ```sh
     sudo systemctl status mysql
     ```

### 4-mysql_configuration_replica

**Description:**
This file contains the MySQL configuration for the replica (slave) database server. It includes settings necessary for enabling replication and optimizing performance.

**Usage Instructions:**

1. **Open the File:**
   - Open the `4-mysql_configuration_replica` file in a text editor to review the configuration.

2. **Apply Configuration:**
   - Copy the configuration settings into your replica MySQL server's configuration file, typically located at `/etc/mysql/mysql.conf.d/mysqld.cnf` or `/etc/my.cnf`.

3. **Restart MySQL Service:**
   - Restart the MySQL service to apply the changes:
     ```sh
     sudo systemctl restart mysql
     ```

4. **Verify Configuration:**
   - Check the MySQL logs and status to ensure the configuration is correctly applied:
     ```sh
     sudo systemctl status mysql
     ```

### 5-mysql_backup

**Description:**
This file contains a script for performing backups of the MySQL database. It ensures that you have a regular backup of your database for disaster recovery.

**Usage Instructions:**

1. **Open the File:**
   - Open the `5-mysql_backup` file in a text editor to review the script.

2. **Set Permissions:**
   - Ensure the script has execute permissions:
     ```sh
     chmod +x 5-mysql_backup
     ```

3. **Run the Script:**
   - Execute the script to perform a backup:
     ```sh
     ./5-mysql_backup
     ```

4. **Verify Backup:**
   - Check the backup location to ensure the backup file is created successfully.

### install_log

**Description:**
This file contains the log of the MySQL installation process. It provides details about the installation steps and any issues encountered.

**Usage Instructions:**

1. **Open the File:**
   - Open the `install_log` file in a text editor to review the installation log.

2. **Review Log:**
   - Examine the log for any errors or warnings during the installation process. Use this information to troubleshoot and resolve any issues.

### replication

**Description:**
This file provides detailed steps and configuration settings for setting up MySQL replication, including both primary and replica configurations.

**Usage Instructions:**

1. **Open the File:**
   - Open the `replication` file in a text editor to review the replication setup instructions.

2. **Follow Steps:**
   - Follow the step-by-step instructions to configure replication on both the primary and replica servers. Ensure you have applied the configurations from `4-mysql_configuration_primary` and `4-mysql_configuration_replica` files.

3. **Verify Replication:**
   - After completing the setup, verify that replication is working correctly by checking the status on both the primary and replica servers:
     ```sh
     SHOW MASTER STATUS;
     SHOW SLAVE STATUS \G;
     ```

### setup.sql

**Description:**
This file contains SQL statements necessary for initializing the MySQL database, such as creating users and granting replication privileges.

**Usage Instructions:**

1. **Open the File:**
   - Open the `setup.sql` file in a text editor to review the SQL statements.

2. **Execute SQL Script:**
   - Log into the MySQL primary server and execute the SQL script:
     ```sh
     mysql -u root -p < setup.sql
     ```

3. **Verify Execution:**
   - Check the MySQL server to ensure the SQL statements have been executed correctly and the necessary users and privileges are set up.

### setup_master

**Description:**
This script contains commands to configure the MySQL server as the primary (master) for replication.

**Usage Instructions:**

1. **Open the File:**
   - Open the `setup_master` file in a text editor to review the commands.

2. **Set Permissions:**
   - Ensure the script has execute permissions:
     ```sh
     chmod +x setup_master
     ```

3. **Run the Script:**
   - Execute the script on the primary MySQL server:
     ```sh
     ./setup_master
     ```

4. **Verify Configuration:**
   - Verify that the primary server is configured correctly for replication:
     ```sh
     SHOW MASTER STATUS;
     ```

### setup_slave

**Description:**
This script contains commands to configure the MySQL server as a replica (slave) for replication.

**Usage Instructions:**

1. **Open the File:**
   - Open the `setup_slave` file in a text editor to review the commands.

2. **Set Permissions:**
   - Ensure the script has execute permissions:
     ```sh
     chmod +x setup_slave
     ```

3. **Run the Script:**
   - Execute the script on the replica MySQL server:
     ```sh
     ./setup_slave
     ```

4. **Verify Configuration:**
   - Verify that the replica server is configured correctly for replication:
     ```sh
     SHOW SLAVE STATUS \G;
     ```

## Conclusion

This directory provides essential configurations and scripts for setting up and managing MySQL databases, including replication and backups. Follow the detailed usage instructions for each file to ensure your MySQL setup is secure, functional, and reliable.
