<properties
    pageTitle="I can't connect to an application on my VM"
    description="I can't connect to an application on my VM "
    service="microsoft.classiccompute"
    resource="virtualmachines"
    authors="ScottAzure"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds="32411838"
    productPesIds="14749"
    resourceTags="windows, linux, WindowsSQL, redhat"
	cloudEnvironments="public, Fairfax, usnat, ussec"	 
 	articleId="57217dbb-3800-492d-8615-8250b02a87ea"
	ownershipId="Compute_VirtualMachines_Content"
/>

# I can't connect to an application on my VM

## **Recommended steps**

First ensure you are able to RDP or SSH to the VM, and then try the following steps:

1. Verify the application is listening on the expected ports and endpoints <br>

    Use the 'netstat -a' command to show active listening ports on the VM and check the endpoint's ACL rules for public and private ports.<br>

2. Test the application access from different VMs:<br>

  Try to access the application from a different virtual machine in the same virtual network, and test from VMs in different subnets. If you cannot access, check the host firewall and network security group configurations.<br>

3. Test external application access:<br>

  Try to access the application from a computer outside the virtual network. If you cannot access it, check the external load balancer configuration, endpoint (TCP or UDP), network security group, and NAT configuration.<br>

## **Recommended documents**

* [About network security groups](https://azure.microsoft.com/documentation/articles/virtual-networks-nsg/)<br>
* [Troubleshoot access to an application running on an azure virtual machine](https://azure.microsoft.com/documentation/articles/virtual-machines-troubleshoot-access-application/)
