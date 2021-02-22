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

Many DNS/AD issues are due to incorrect or unsupported network configurations. When you encounter connectivity issues, make sure that your network configuration and Vnet peering follows the supported configurations by reviewing these [Guidelines for Azure NetApp Files network planning](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-network-topologies). 

## **Recommended Steps**

The following details apply to the Continuously Available Share Feature in SMB volume:
-  The CA Share feature is supported in SMBv3 or later, and is available in Windows 8, Windows Server 2012 and later versions.
-  Make sure that this feature is enabled only for Microsoft SQL server workloads. This feature can reduce performance if used for non-Microsoft SQL Server workloads. The impact can include other volumes in the same ONTAP cluster.

## **Recommended Documents**

- [SMB FAQs](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-faqs#smb-faqs)<br>
- [Create an SMB volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb)<br>

