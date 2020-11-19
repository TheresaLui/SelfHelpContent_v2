<properties
	pageTitle="Currently recovery of ADLS Gen 2 File system isn't supported"
	description="Currently recovery of ADLS Gen 2 File system isn't supported"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="61814b58-0c40-4aea-902f-d8cd91a3cee3"
/>

# ADLS Gen 2 Recovery

<!--issueDescription-->

1. There is no change in terms of **ADLS Gen2 Accounts**. Follow the same process as that of General Purpose accounts <br>
2. For **BLOBS** and **CONTAINERS**, continue to file an ICM to xstore\bigdata as appropriate.
4. To prevent this, you can leverage on Backup and archive solutions in Azure, enabling Azure Soft Delete for Blobs or Azure Blob Snapshots.<br>
5. Currently recovery of **ADLS Gen 2 File system** isn't supported<br>


<!--/issueDescription-->