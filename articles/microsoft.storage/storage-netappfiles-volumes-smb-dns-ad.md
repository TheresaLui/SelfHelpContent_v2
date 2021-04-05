<properties
  pagetitle="Common NetApp Volumes Issues SMB, DNS, Active Directory&#xD;"
  description="Issues with SMB, DNS, Active Directory"
  service="microsoft.storage"
  resource="storage"
  ms.author="b-avaish,b-mayada"
  selfhelptype="Generic"
  supporttopicids="32740758"
  resourcetags=""
  productpesids="16469"
  cloudenvironments="public,mooncake,fairfax,blackforest,usnat,ussec"
  articleid="netappvolumesissuesmbdnsad"
  ownershipid="AzureNetAppFiles" />
# Common NetApp Volumes Issues SMB, DNS, Active Directory

## DNS and AD Connectivity Issues

Many DNS/AD issues are due to incorrect or unsupported network configurations. When you encounter connectivity issues, make sure that your network configuration and VNet peering follows the supported configurations by reviewing these [Guidelines for Azure NetApp Files network planning](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-network-topologies). 

## **Recommended Steps**

The following details apply to the Continuously Available Share feature in SMB volume:
-  The CA Share feature is supported in SMBv3 or later, and is available in Windows 8, Windows Server 2012 and later versions.
-  Make sure that this feature is enabled only for Microsoft SQL server workloads. It can reduce performance if used for non-Microsoft SQL Server workloads. The impact can include other volumes in the same ONTAP cluster.

The following details apply to the LDAP Extended Group feature in NFS volume: 
-  Refer to [troubleshoot-LDAP-volumes](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-ldap-volumes) if you are getting Error while creating LDAP Volume
-  If you're using [LDAP with Extended Group for the volume](https://docs.microsoft.com/azure/azure-netapp-files/configure-ldap-extended-groups),  check if you want to [allow local NFS User with LDAP UI](https://docs.microsoft.com/azure/azure-netapp-files/create-volumes-dual-protocol#allow-local-nfs-users-with-ldap-to-access-a-dual-protocol-volume)


## **Recommended Documents**

- [SMB FAQs](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-faqs#smb-faqs)<br>
- [Create an SMB volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb)<br>
- [Creating NFS Volumes with LDAP Extended Group](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes) and [Configuring LDAP with Extended Group for the volume](https://docs.microsoft.com/azure/azure-netapp-files/configure-ldap-extended-groups)
- [Configuring LDAP with Extended Group for the volume](https://docs.microsoft.com/azure/azure-netapp-files/configure-ldap-extended-groups)
