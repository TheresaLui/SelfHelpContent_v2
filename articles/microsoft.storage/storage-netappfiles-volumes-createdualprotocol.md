<properties
	pageTitle="Issue while creating dual protocol volume"
	description="Issue while creating dual protocol volume"
	service="microsoft.storage"
	resource="storage"
	authors="b-kiudup"
	ms.author="b-kiudup"
	displayOrder=""
	articleId="NetAppVolumesIssuecreatedualprotocol"
	selfHelpType="generic"
	supportTopicIds="32777923"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# NetApp Volumes Issue while creating dual protocol volume

## **Recommended Steps**

1. Make sure that Active Directory is running and the specified DNS servers must be reachable from the delegated subnet of Azure NetApp Files. 
2. Make sure proper root certificate is added in AD connection in NetApp account and reverse lookup zones are updated. Refer to [Troubleshoot dual protocol volumes](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-dual-protocol-volumes) for more information.

## **Recommended Documents**

- [Create Dual protocol volumes using Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/create-volumes-dual-protocol)<br>
- [Troubleshoot Dual protocol volume creation issues](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-dual-protocol-volumes)<br>
- [Guidelines for Azure NetApp Files network planning](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-network-topologies)<br>
