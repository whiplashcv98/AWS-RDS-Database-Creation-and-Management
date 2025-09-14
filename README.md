# AWS-RDS-Database-Creation-and-Management
This project outlines the step-by-step process of creating and managing a Relational Database Service (RDS) instance on Amazon Web Services (AWS). It covers key configuration steps, including backup, maintenance, and deletion protection, and demonstrates how to connect to the database using an external SQL client like MySQL Workbench.
An excellent project title would be "AWS RDS Database Creation and Management." Here is a professional README based on the information provided.

Core Components
Amazon Relational Database Service (RDS): A managed relational database service that simplifies the setup, operation, and scaling of a relational database in the cloud.

Security Groups: Act as a virtual firewall for the RDS instance, controlling inbound and outbound traffic.

MySQL Workbench: A unified visual tool for database architects, developers, and DBAs to perform SQL development, database design, creation, and maintenance.

Step-by-Step Implementation
Backup Configuration:

Set the backup retention period (e.g., 1 day) to specify how long to keep automated backups.

Set the backup window to "No preference."

Maintenance Configuration:

Enable auto minor version upgrade to automatically apply updates.

Set the maintenance window to "No preference."

Deletion Protection:

Turn off Enable deletion protection for this tutorial to allow for easy deletion later.

Proceed to Create Database.

Database Instance Creation:

The database instance will have a status of creating for several minutes.

Once the status changes to available, it is ready to be connected to.

Connecting with MySQL Workbench:

Download and install MySQL Workbench.

Ensure you run MySQL Workbench from the same device used to create the DB instance, as the security group is configured to only allow connections from that device.

After a successful connection, you can see the database schema and objects.

Executing a SQL Script:

Execute the following SQL script to create a sample table:

SQL

CREATE TABLE `employee` ( 
`id` int NOT NULL AUTO_INCREMENT, 
`name` varchar(255) DEFAULT NULL,
`email` varchar(255) DEFAULT NULL,
`city` varchar(255) DEFAULT NULL, 
PRIMARY KEY (`id`)
);
Deleting the RDS Database:

Go back to the Amazon RDS console, select the database instance, and choose Delete from the Actions dropdown menu.

Confirm the deletion and choose not to create a final snapshot.








