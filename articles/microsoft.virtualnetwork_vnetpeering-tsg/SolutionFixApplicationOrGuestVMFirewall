<properties
	pageTitle="SolutionGuestApplicationOrFirewall"
	description="SolutionGuestApplicationOrFirewall"
	service="microsoft.network"
	resource="virtualNetworks/virtualNetworkPeerings"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32589558,32584249"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="SolutionGuestApplicationOrFirewall"
/>

# VM Application not listening or OS firewall blocking traffic

This issue is caused by the VM configuration in the <application/firewall> that was not enabling network traffic to reach the application. By default, VM applications need to be configured to listen on particular TCP/UDP ports to receive the requests from the networking layer. A firewall rule must also be configured to allow this traffic through. 

## **Recommended Steps**

1. Ensure the application service is running and listening on the expected port

   1. Windows: Use the command ***netstat -ano | findstr LISTENING | findstr 3389*** where 3389 is the port number you expect the computer to be listening on.
   2. Linux: ***netstat -ano | grep LISTEN | grep 22*** where 22 is the port number you expect the computer to be listiening on.

2. Ensure the Guest OS firewall is allowing network traffic on the application port configured.

## **Recommended Documents**

* [Check whether VM app or service is listening on the port](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms#step-4-check-whether-vm-app-or-service-is-listening-on-the-port)
* [Disable the guest OS Firewall on Azure VM](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/disable-guest-os-firewall-windows)
