<properties
	pageTitle="Issue while mounting dual protocol volume"
	description="Issue while mounting dual protocol volume"
	service="microsoft.storage"
	resource="storage"
	authors="b-kiudup"
	ms.author="b-kiudup"
	displayOrder=""
	articleId="NetAppVolumesIssuemountdualprotocol"
	selfHelpType="generic"
	supportTopicIds="32777925"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# NetApp Volumes Issue while mounting dual protocol volume

## **Recommended Steps**

1. Make sure that Active Directory is running and the specified DNS servers must be reachable from the delegated subnet of Azure NetApp Files. 
2. Make sure proper root certificate is added in AD connection in NetApp account and reverse lookup zones are updated. Refer to [Troubleshoot dual protocol volumes](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-dual-protocol-volumes) for more information.
3. Ensure that the NFS client is up to date and running the latest updates for the operating system. Refer to [Configure an NFS client for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/configure-nfs-clients) for more information.

## **Recommended Documents**

- [Create Dual protocol volumes using Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/create-volumes-dual-protocol)<br>
- [Troubleshoot Dual protocol volume creation issues](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-dual-protocol-volumes)<br>
- [Guidelines for Azure NetApp Files network planning](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-network-topologies)<br>
- [Configure export policy for an NFS volume](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-configure-export-policy)<br>
