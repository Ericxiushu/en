# Associate Elastic IP

## Operation Steps

1. Access [Virtual Machine Console](https://cns-console.jdcloud.com/host/compute/list) and enter the instance list page. Or access [JD Cloud Console](https://console.jdcloud.com) Click navigation bar on the left [Elastic Compute] - [Virtual Machine] to enter the instance list page.
2. Select Regions.
3. In the instance list, select the instance to which you want to associate elastic IP. Click the name to enter the details page.
4. Click [Elastic Network Interface] Tab, select the elastic network interface that needs to be associated to the elastic IP, find the private IP to be associated, and click [Elastic IP].
5. In the pop-up window, select public IP of the disassociated resource and click [Confirm].
		
		Please note:
		* The secondary network interface is not allowed to associate the public IP of the single availability zone;
		* Associating EIP on the list page is the primary private IP associated with the primary network interface of virtual machine.
		
In addition, you can also:

* Associate elastic IP to the primary private IP of the primary network interface instance on the instance list page. The operation steps are as follows:
	1. Access [Virtual Machine Console](https://cns-console.jdcloud.com/host/compute/list) and enter the instance list page. Or access [JD Cloud Console](https://console.jdcloud.com) Click navigation bar on the left [Elastic Compute] - [Virtual Machine] to enter the instance list page.
	2. Select Regions.
	3. In the instance list, select an instance of the elastic IP to be associated to the primary private IP of the primary network interface. Click Associate EIP.
	5. In the pop-up window, select public IP of the disassociated resource and click [Confirm].
	 
* Associate operation from the elastic network interface console. For details, see [Elastic Network Interface Side Associate EIP](../../../../Networking/Elastic-Network-Interface/Operation-Guide/ Private-IP-Management/Associate-Elastic-IP.md).

## Related Reference

[Elastic Network Interface Side Associate EIP](../../../../Networking/Elastic-Network-Interface/Operation-Guide/Private-IP-Management/Associate-Elastic-IP.md)