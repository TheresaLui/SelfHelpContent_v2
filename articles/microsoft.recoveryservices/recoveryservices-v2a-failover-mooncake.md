<properties
	pageTitle="Site Recovery (VMware to Azure)/Failover: Unplanned failover"
	description="Site Recovery (VMware to Azure)/Failover: Unplanned failover"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="prateek9us"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536465"
	resourceTags=""
	productPesIds="16370"
	cloudEnvironments="MoonCake, Fairfax"
	articleId="ea71eda1-8ece-4c47-958f-3c9de25c8200"
	ownershipId="Compute_SiteRecovery"
/>

# Site Recovery (VMware to Azure)/Unable to connect/RDP/SSH to the failed over virtual machine

## **Recommended steps**

**Connect button is grayed out on the virtual machine** 
- If the deployment model is Resource Manager <br/>
Add a Public IP on the Network interface of the virtual machine. [See the steps to add a public ip here](https://docs.azure.cn/site-recovery/site-recovery-monitoring-and-troubleshooting#adding-a-public-ip-on-a-resource-manager-virtual-machine)<br/>
- If the deployment model is Classic <br/>
Add an endpoint on public port 3389 for RDP and on public port 22 for SSH. [See the steps to add an endpoint here](https://docs.azure.cn/virtual-machines/windows/classic/setup-endpoints)<br/>

**Connect button is available on the virtual machine**
- Look at the console screenshot of the virtual machine by going to **Boot diagnostics** in the virtual machine menu.  Boot diagnostics is enabled by default on a Resource Manager virtual machine. You need to manually enable it on a Classic virtual machine. <br/>
	- Note that enabling any setting other than Boot Diagnostics would require Azure VM Agent to be installed in the virtual machine before the failover<br/>
- If the virtual machine has not started, try failing over to an older recovery point by using **Change Recovery Point** option on the virtual machine<br/>
- If the application inside the virtual machine is not coming up, try failing over to an app-consistent recovery point by using **Change Recovery Point** option on the virtual machine<br/>
- If the virtual machine is domain joined then ensure that domain controller is correctly functioning. You can do that by creating a new virtual machine in the same network and ensuring that it is able to join to the same domain on which the failed over virtual machine is expected to come up<br/>
	- If the domain controller is not functioning correctly try logging in to the failed over virtual machine using a local administrator account<br/>
- If you are using a custom DNS server then ensure that it is reachable. You can do that by creating a new virtual in the same network and checking that it is able to do name resolution using the custom DNS Server<br/>

## **Recommended documents**

[Detailed failover documentation](https://docs.azure.cn/site-recovery/site-recovery-failover)<br/>
[Troubleshoot RDP connection](https://docs.azure.cn/virtual-machines/windows/troubleshoot-rdp-connection)<br/>
