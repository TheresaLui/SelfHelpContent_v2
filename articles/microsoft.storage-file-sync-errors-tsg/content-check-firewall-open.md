<properties
	pageTitle="How to check the firewall is open for port 443"
	description="How to check the firewall is open for port 443"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7d66ed88-82f0-49ef-b94e-9cdb757205d0"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check the firewall is open for port 443

1. If the server is behind a firewall, verify port 443 outbound is allowed.
2. If the firewall restricts traffic to specific domains, confirm the domains listed in the [Firewall documentation are accessible](https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-firewall-and-proxy#firewall)
