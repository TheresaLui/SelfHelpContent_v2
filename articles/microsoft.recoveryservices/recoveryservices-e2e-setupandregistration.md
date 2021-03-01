<properties
  pagetitle="Site Recovery (VMM to VMM)/Site Recovery provider setup and registration&#xD;"
  description="Site Recovery (VMM to VMM)/Site Recovery provider setup and registration"
  service="microsoft.recoveryservices"
  resource="vaults"
  ms.author="sharrai"
  selfhelptype="Generic"
  supporttopicids="32786263"
  resourcetags=""
  productpesids="16370"
  cloudenvironments="fairfax,mooncake,public,usnat,ussec,blackforest"
  disableclouds=""
  articleid="43c7077b-dfc3-40b1-975f-37f8ed55ec27"
  ownershipid="Compute_SiteRecovery" />
# Site Recovery (VMM to VMM)/Site Recovery provider setup and registration

## **Recommended Steps**

Common issues during Setup & Registration </br>
- Ensure that the server on which you install the **Microsoft Azure Site Recovery Provider** has access to the following url's<br>
	1. *.hypervrecoverymanager.windowsazure.com</br>
	2. *.accesscontrol.windows.net</br>
	3. *.store.core.windows.net</br>
- Ensure that the system clock on the server where you install **Microsoft Azure Site Recovery Provider** has the correct time for the time zone the server is configured for.</br>
- Always choose the 'Connect to Azure Site Recovery using a proxy server' option if you know that the server on which you are installing **Microsoft Azure Site Recovery Provider** is behind a proxy server.<br>
	- This setting can be change at any point of time by running the **DRConfigurator.exe** and re-registering the Microsoft Azure Site Recovery Provider.</br>

## **Recommended  Documents**

[On-premises prerequisites](https://azure.microsoft.com/documentation/articles/site-recovery-vmm-to-vmm/#on-premises-prerequisites)</br>