# Instance Template Overview (in beta)
The instance template is the configuration information template for the instance creation provided by JD Cloud, including the image, instance type, type and capacity of system disk and data disk, virtual private cloud and subnet configuration, security group, and login information, etc. Instance templates can be used to create instances and to configure availability groups, and instance templates must be specified when creating  availability groups. You don't have to re-specify the parameters that are included in the instance template each time you create an instance, which can shorten the deployment time.
	
	Please Note: Once an instance template is created, its attributes will not be editable.

The instance template includes the following instance information:

Information Item | Detailed description
:---|:---
Region | The physical deployment location of instances and other resources.
Image | Instance preset environment, including the server's pre-configured environment (operating system and other installed software).
Instance Type | Identify the corresponding computing, memory, storage, and network capabilities that determine the hardware configuration of the instance
Disk Information|System disk and data disk information.
Network | Virtual private cloud has customized virtual network space to achieve logical isolation between resources. You should specify a virtual private cloud and corresponding subnet for the instance. The Private IP address will be assigned to the instance within the CIDR range.
Elastic IP | It provides the public network access capability for the instance, which can be created with the instance and can be associated separately after creation. The instance template supports not configuring EIP.
Login information | Information of instance login password and key pair, where the Linux system supports specifying key pair for login.

Once the instance template is configured successfully, you can quickly create instances with the same configuration repeatedly, without the instance configuration parameters re-specifying, which could save your time in deployment.

Create an instance by using an instance template: Initialize with the configuration in the instance template by default. You should specify the configuration information that is not included in the instance template, such as availability zone, billing type, etc. You can also make changes if the configuration in the instance template does not meet your creation. It is important to note that the configuration modifying only affects this creation and does not affect the content of the instance template. Please refer to [Create Instance](../Instance/Create-Instance.md) for detailed operation steps.

Select an instance template to create a availability group: Instance templates must be specified when creating availability groups. The newly created instance configuration in the availability group shall be consistent with the instance template configuration, and the availability zone shall be selected according to the availability group configuration. Please refer to [Availability Group](../../../Availability-Group/Introduction/Overview.md) for details.

## Usage Restrictions

* A maximum of 25 instance templates can be created in a single region, please open a ticket application if additional requirements arise;
* The instance template temporarily does not support modification for the time being, if you need to modify some of the information items, we recommend you create a new instance template;
* If the instance template has been referenced by a availability group, the instance template cannot be deleted;
* If the resources referenced by the instance template are deleted, the instance template will not work properly. If the availability group configured with this instance template cannot add new instances normally, you shall make sure that the resources associated with the instance template are available prior to using it.

