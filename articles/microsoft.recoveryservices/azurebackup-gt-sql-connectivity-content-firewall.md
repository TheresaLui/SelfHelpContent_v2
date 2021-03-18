<properties
	  pageTitle="Fix the FireWall and Proxy settings"
	  description="Fix the FireWall and Proxy settings"
      service="Microsoft.RecoveryServices"
      resource="Microsoft.RecoveryServices/vaults"
	  authors="chgonugu"
	  ms.author="chgonugu"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="8e0f2c5a-602c-44da-915b-8724cd6bfd3a"
	  ownershipId="StorageMediaEdge_Backup"
/>

# Fix the Firewall and Proxy settings

Fix the Firewall, Anti virus and Proxy settings to allow outbound connectivity to Azure Backup, Azure Storage and Azure Active Directory Services by whitelisting the IP ranges for these Service tags. The IP ranges for the Service tags are available below.
Public Cloud: https://www.microsoft.com/download/confirmation.aspx?id=56519 
US Government Cloud: https://www.microsoft.com/download/details.aspx?id=57063 
China Cloud: https://www.microsoft.com/download/details.aspx?id=57062 
Germany Cloud: https://www.microsoft.com/download/details.aspx?id=57064 

Alternatively, whitelist the following FQDNs for Azure services
Azure Backup:	*.backup.windowsazure.com
Azure Storage:	*.blob.core.windows.net, *.queue.core.windows.net
Azure AD: Allow access to FQDNs under sections 56 and 59 according to this https://docs.microsoft.com/microsoft-365/enterprise/urls-and-ip-address-ranges?view=o365-worldwide#microsoft-365-common-and-office-online

