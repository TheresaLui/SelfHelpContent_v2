<properties
	pageTitle="Site Recovery (Hyper-V Site to Azure)/Add new servers to Hyper-V site"
	description="Site Recovery (Hyper-V Site to Azure)/Add new servers to Hyper-V site"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="anoopkv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32536385"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
/>

# Site Recovery (Hyper-V Site to Azure)/Add new servers to Hyper-V site

Common issues during adding servers to Hyper-V Site

## **Recommended Steps**

*  Ensure that the installation is done using an account that is a **Local Administrator** on the server.
* Ensure that the server on which you install the **Microsoft Azure Site Recovery Provider** has access to the following url's <br>
	1. *.hypervrecoverymanager.windowsazure.cn
	2. *.accesscontrol.chinacloudapi.cn
	3. *.backup.windowsazure.cn
	4. *.blob.core.chinacloudapi.cn
	5. *.store.core.chinacloudapi.cn

* Ensure that the system clock on the server where you install **Microsoft Azure Site Recovery Provider** has the correct time for the time zone the server is configured for.

* Always choose the 'Connect to Azure Site Recovery using a proxy server' option if you know that the server on which you are installing **Microsoft Azure Site Recovery Provider** is behind a proxy server.

* The **Microsoft Azure Site Recovery Provider** should not be installed on a Domain Controller


## **Recommended  Documents**
[On-premises prerequisites](https://docs.azure.cn/site-recovery/hyper-v-site-walkthrough-overview#on-premises-prerequisites)
