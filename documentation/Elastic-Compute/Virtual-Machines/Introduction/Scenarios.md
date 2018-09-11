# Application Scenario
## Enterprise Website/Web Application/Mobile APP
* Scenario Description: For the initial stage of such applications, the traffic is usually small, and the lightweight deployment scheme is adopted. The smaller instance specifications and low-bandwidth instance configurations can meet the business requirements and realize the operation of applications, databases, and other services. With the increasing visits to the websites/applications and the diversification of services, the cloud server specifications and scale can be quickly adjusted, and the resource ratio can be flexibly adjusted according to the business cycle to obtain elastic improvement of the computing power at a small cost.
* Recommended Configuration: virtual machine and load balancer; instance type of g.s1.micro (1-core, 1GB) and elastic IP bandwidth of 1Mbps.
*
![](../../../../image/vm/Scenarios-Web.png)

## Mass Images/Video Applications

* Scenario Description: In actual mass picture/video applications, for example,  large E-commerce websites, it is recommended to use object storage service to store your static pictures, videos and other data, and use CDN and load balancer at the same time, which can greatly reduce user's costs while reducing the access waiting time.
* Recommended Configuration: virtual machine, load balancer, object storage service, CDN and database; instance type of g.n2.medium (2-core, 4GB) and EIP bandwidth of 5Mbps.
*
![](../../../../image/vm/Scenarios-Image.png)
