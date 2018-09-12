# Security

## Instance Login Credential Configuration

The instance login credentials include the login password and the key pair.

For Linux instances, it is recommended to login to the instance using key pair.

For Windows instances, it is recommended to change the password periodically and try to increase the password strength to avoid the risk of brute force attack caused by weak passwords. The password is recommended to be in at least 8 digits, whose complexity shall be increased from the type of characters, such as letters in uppercase and lowercase, numbers and special characters.

## System Vulnerability Protection

For system vulnerabilities, it is recommended to periodically resolve them through system patches. For Linux system, tasks should be set regularly to execute yum update -y to update system packages and kernels. For Windows system, the patch update is recommended to be always enabled.

## Account Access Management
When multiple different accounts are required to control a same set of instance, the user can use its access to cloud through [Identity and Access Management](../../../Management-and-Monitoring/IAM/Overview.md).

## Division of Virtual Private Cloud

Choose to use virtual private cloud to divide logical areas, deploy instances of different business attributes in different virtual private cloud, or in different subnets of a same virtual private cloud, and configure the identity and access management between subnets through network ACL to isolate instances at different security levels inside the enterprise. For more information, please refer to [Virtual Private Cloud](../../../Networking/Overview.md).

## Security Group Configuration

When using a security group, it is recommended to configure the security group according to principle.

* Minimum Authorization.

	Restrict the access by using the allowed trusted address of security group to access instances. Configure the strictest rules in security group. Since the security group employs a white list mechanism, you only need to open the traffic port configuration that allows access.
	
	For example, you can configure that only allowing your local host to access the TCP inbound traffic of port 80. If your local host's public IP address is 111.111.111.111, you can add a security group rule with source of 111.111.111.111, protocol of TCP and destination port of 80. Please refer to the security group for more information.
* Create and Apply Different Security Groups on Instance Sets of Different Services.

	For example, you should use different security groups for the Web, Service, Database, and Cache layers, and expose different access rules and permissions to ensure that instances of different important businesses cannot be easily accessed from outside to ensure business security.
* Do Not Use Network Access Rule of 0.0.0.0/0.

	Opening 0.0.0.0/0 means that all ports are exposed, which is very dangerous. The principle of minimum authorization should be referred and only a minimum number of ports should be opened. For example, for Web server, only ports 80, 8080 and 443 should be opened.
	
* Delete Unnecessary Security Groups.
Security rules in a security group are similar to a white list. Therefore, please do not keep unnecessary security groups to avoid unnecessary troubles caused by adding an instance by error.
