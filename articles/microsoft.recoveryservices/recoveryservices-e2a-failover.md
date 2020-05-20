<properties
	pageTitle="Site Recovery (VMM to Azure)/Failover: Planned and unplanned failover"
	description="Site Recovery (VMM to Azure)/Failover: Planned and unplanned failover"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="prateek9us"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536427"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="f5a0447b-c681-4d9d-8c00-19c217e3d3ed"
	ownershipId="Compute_SiteRecovery"
/>

# Site Recovery (VMM to Azure)/Unable to connect/RDP/SSH to the failed over virtual machine

## **Recommended Steps**

**Connect button is grayed out on the virtual machine**<br/>
- If the deployment model is Resource Manager <br/>
Add a Public IP on the Network interface of the virtual machine. [See the steps to add a public ip here](https://aka.ms/asr-resourcemanager-vm-connect)<br/>
- If the deployment model is Classic <br/>
Add an endpoint on public port 3389 for RDP and on public port 22 for SSH. [See the steps to add an endpoint here](https://aka.ms/asr-classic-vm-connect)<br/>

**Connect button is available on the virtual machine**<br/>
- Look at the console screenshot of the virtual machine by going to **Boot diagnostics** in the virtual machine menu.  Boot diagnostics is enabled by default on a Resource Manager virtual machine. You need to manually enable it on a Classic virtual machine. <br/>
	- Note that enabling any setting other than Boot Diagnostics would require Azure VM Agent to be installed in the virtual machine before the failover<br/>
- If the virtual machine has not started, try failing over to an older recovery point by using **Change Recovery Point** option on the virtual machine<br/>
- If the application inside the virtual machine is not coming up, try failing over to an app-consistent recovery point by using **Change Recovery Point** option on the virtual machine<br/>
- If the virtual machine is domain joined then ensure that domain controller is correctly functioning. You can do that by creating a new virtual machine in the same network and ensuring that it is able to join to the same domain on which the failed over virtual machine is expected to come up<br/>
	- If the domain controller is not functioning correctly try logging in to the failed over virtual machine using a local administrator account<br/>
- If you are using a custom DNS server then ensure that it is reachable. You can do that by creating a new virtual in the same network and checking that it is able to do name resolution using the custom DNS Server<br/>

## **Recommended documents**

[Detailed failover documentation](https://azure.microsoft.com/documentation/articles/site-recovery-failover/)<br/>
[Troubleshoot RDP connection](https://azure.microsoft.com/documentation/articles/virtual-machines-windows-troubleshoot-rdp-connection/)<br/>
