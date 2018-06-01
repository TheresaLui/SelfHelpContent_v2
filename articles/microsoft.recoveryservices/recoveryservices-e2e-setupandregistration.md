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
	productPesIds="16370"
	cloudEnvironments="public"
/>

# Site Recovery (VMM to VMM)/Site Recovery provider setup and registration
## **Recommended Steps**
Common issues during Setup & Registration

* Ensure that the server on which you install the **Microsoft Azure Site Recovery Provider** has access to the following url's<br>
	1. *.hypervrecoverymanager.windowsazure.com
	2. *.accesscontrol.windows.net
	3. *.store.core.windows.net

* Ensure that the system clock on the server where you install **Microsoft Azure Site Recovery Provider** has the correct time for the time zone the server is configured for.


* Always choose the 'Connect to Azure Site Recovery using a proxy server' option if you know that the server on which you are installing **Microsoft Azure Site Recovery Provider** is behind a proxy server.<br>
	* This setting can be change at any point of time by running the **DRConfigurator.exe** and re-registering the Microsoft Azure Site Recovery Provider.


## **Recommended  Documents**
[On-premises prerequisites](https://azure.microsoft.com/documentation/articles/site-recovery-vmm-to-vmm/#on-premises-prerequisites)
