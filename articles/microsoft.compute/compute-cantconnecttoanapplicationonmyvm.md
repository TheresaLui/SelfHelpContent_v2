<properties  
	pageTitle="I can't connect to an application on my VM"
	description="I can't connect to an application on my VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="kasparks"
	displayOrder="6"
	selfHelpType="resource"
	supportTopicIds="32411838"
	resourceTags="windows, linux, windowsSQL, redhat, Ubuntu"	 
	productPesIds="14749"
	cloudEnvironments="public"
/>
    
# I can't connect to an application on my VM

## **Recommended steps**
First ensure you are able to RDP or SSH to the VM and then try the following steps.

1. Verify the application is listening on the expected ports and endpoints <br>
Use 'netstat -a' to show the active listening ports on the VM and check the endpoints ACL rules for public and private ports
2. Test application access from different VMs <br>
Try to access the application from a different virtual machine in the same virtual network, and test the VMs in different subnets. If you can't access it, check the host firewall and [network security group configurations](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade).
3. Test external application access <br>
Try to access the application from a computer outside of the virtual network. If you can't access it, check the external load balancer configuration, endpoint (TCP or UDP), [network security group](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade), and NAT configuration.

## **Recommended documents**
[About network security groups](https://azure.microsoft.com/documentation/articles/virtual-networks-nsg/) <br>
[Troubleshoot access to an application running on an Azure virtual machine](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-access-application/)
