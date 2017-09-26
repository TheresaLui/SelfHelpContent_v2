<properties
	pageTitle="Site Recovery (VMM to VMM)/Site Recovery provider setup and registration"
	description="Site Recovery (VMM to VMM)/Site Recovery provider setup and registration"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536454"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
/>

# Site Recovery (VMM to VMM)/Site Recovery provider setup and registration
## **Recommended Steps**
Common issues during Setup & Registration

* Ensure that the server on which you install the **Microsoft Azure Site Recovery Provider** has access to the following url's<br>
	1. *.hypervrecoverymanager.windowsazure.cn
	2. *.accesscontrol.chinacloudapi.cn
	3. *.store.core.chinacloudapi.cn

* Ensure that the system clock on the server where you install **Microsoft Azure Site Recovery Provider** has the correct time for the time zone the server is configured for.


* Always choose the 'Connect to Azure Site Recovery using a proxy server' option if you know that the server on which you are installing **Microsoft Azure Site Recovery Provider** is behind a proxy server.<br>
	* This setting can be change at any point of time by running the **DRConfigurator.exe** and re-registering the Microsoft Azure Site Recovery Provider.


## **Recommended  Documents**
[On-premises prerequisites](https://docs.azure.cn/site-recovery/site-recovery-vmm-to-vmm#on-premises-prerequisites)
