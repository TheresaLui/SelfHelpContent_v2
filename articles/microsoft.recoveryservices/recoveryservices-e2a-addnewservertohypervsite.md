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
	productPesIds="16370"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="149aa758-e4a5-473b-8a18-4a4376439aa0"
	ownershipId="Compute_SiteRecovery"
/>

# Site Recovery (VMM to Azure)/Site Recovery provider setup and registration

## **Recommended Steps**

- Ensure that the installation is done using an account that is a **Local Administrator** on the server. </br>
- Ensure that the server on which you install the **Microsoft Azure Site Recovery Provider** has access to the following url's <br>
	1. *.hypervrecoverymanager.windowsazure.com</br>
	2. *.accesscontrol.windows.net</br>
	3. *.backup.windowsazure.com</br>
	4. *.blob.core.windows.net</br>
	5. *.store.core.windows.net</br>
- Ensure that the system clock on the server where you install **Microsoft Azure Site Recovery Provider** has the correct time for the time zone the server is configured for.</br>
- Always choose the 'Connect to Azure Site Recovery using a proxy server' option if you know that the server on which you are installing **Microsoft Azure Site Recovery Provider** is behind a proxy server.</br>

## **Recommended  Documents**

[On-premises prerequisites](https://azure.microsoft.com/documentation/articles/site-recovery-vmm-to-azure/#on-premises-prerequisites)</br>
