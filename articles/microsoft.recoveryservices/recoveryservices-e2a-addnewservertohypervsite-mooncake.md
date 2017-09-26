<properties
	pageTitle="Site Recovery (VMM to Azure)/Site Recovery provider setup and registration"
	description="Site Recovery (VMM to Azure)/Site Recovery provider setup and registration"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536453"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
/>

# Site Recovery (VMM to Azure)/Site Recovery provider setup and registration

Common issues during adding servers to Hyper-V Site

## **Recommended Steps**

*  Ensure that the installation is done using an account that is a **Local Administrator** on the server.
* Ensure that the server on which you install the **Microsoft Azure Site Recovery Provider** has access to the following url's <br>
	1. *.hypervrecoverymanager.windowsazure
	2. *.accesscontrol.chinacloudapi.cn
	3. *.backup.windowsazure
	4. *.blob.core.chinacloudapi.cn
	5. *.store.core.chinacloudapi.cn

* Ensure that the system clock on the server where you install **Microsoft Azure Site Recovery Provider** has the correct time for the time zone the server is configured for.

* Always choose the 'Connect to Azure Site Recovery using a proxy server' option if you know that the server on which you are installing **Microsoft Azure Site Recovery Provider** is behind a proxy server.

## **Recommended  Documents**
[On-premises prerequisites](https://docs.azure.cn/site-recovery/site-recovery-vmm-to-azure#on-premises-prerequisites)
