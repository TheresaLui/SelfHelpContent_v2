<properties
	pageTitle="Site Recovery (VMM to Azure)/Failover: Test failover"
	description="Site Recovery (VMM to Azure)/Failover: Test failover"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="prateek9us"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536461"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public"
/>

# Site Recovery (VMM to Azure)/Failover: Test failover

## **Unable to connect/RDP/SSH to the failed over virtual machine**

### **Connect button is grayed out on the virtual machine** 
* If the deployment model is Resource Manager <br/>
Add a Public IP on the Network interface of the virtual machine. [See the steps to add a public ip here](https://aka.ms/asr-resourcemanager-vm-connect)


* If the deployment model is Classic <br/>
Add an endpoint on public port 3389 for RDP and on public port 22 for SSH. [See the steps to add an endpoint here](https://aka.ms/asr-classic-vm-connect)

### **Connect button is available on the virtual machine**
* Look at the console screenshot of the virtual machine by going to **Boot diagnostics** in the virtual machine menu.  Boot diagnostics is enabled by default on a Resource Manager virtual machine. You need to manually enable it on a Classic virtual machine. 
	* Note that enabling any setting other than Boot Diagnostics would require Azure VM Agent to be installed in the virtual machine before the failover

* If the virtual machine has not started, try failing over to an older recovery point

* If the application inside the virtual machine is not coming up, try failing over to an app-consistent recovery point

* If the virtual machine is domain joined then ensure that domain controller is correctly functioning. You can do that by creating a new virtual machine in the same network and ensuring that it is able to join to the same domain on which the failed over virtual machine is expected to come up

	* If the domain controller is not functioning correctly try logging in to the failed over virtual machine using a local administrator account
	
	
* If you are using a custom DNS server then ensure that it is reachable. You can do that by creating a new virtual in the same network and checking that it is able to do name resolution using the custom DNS Server


## **Recommended documents**
[Detailed failover documentation](https://azure.microsoft.com/documentation/articles/site-recovery-failover/)

[Troubleshoot RDP connection](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-troubleshoot-rdp-connection/)
