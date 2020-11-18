<properties
	pageTitle="Issues with SMB, DNS Active Directory"
	description="Issues with SMB, DNS, Active Directory"
	service="microsoft.storage"
	resource="storage"
	authors="b-avaish"
	ms.author="b-avaish"
	displayOrder=""
	articleId="NetAppVolumesIssueSMBDNSAD"
	selfHelpType="generic"
	supportTopicIds="32740758"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# Common NetApp Volumes Issues SMB, DNS, Active Directory

## DNS and AD Connectivity Issues

Many DNS/AD issues are due to incorrect or unsupported network configurations.  When you encounter connectivity issues, please review the [Guidelines for Azure NetApp Files network planning](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-network-topologies) document and make sure your network configuration and Vnet peering follows the supported configurations. 

## **Recommended Steps for Continuously Available Share Feature in SMB volume**
1.Make sure that subscription is whitelisted for ANFSMBCAShare Afec.
2.Note that CA Share feature is supported in SMB3 or later versions and is available in windows 8, windows server 2012 or later versions.
3.Make sure that this feature is enabled only for Microsoft SQL server workloads since this can have performance impact (even on other volumes in the same ONTAP cluster) if used for non-Microsoft SQL server workloads.
## **Recommended Documents**

- [SMB FAQs](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-faqs#smb-faqs)<br>
- [Create an SMB Volumes for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb)<br>

