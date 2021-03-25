<properties
  pagetitle="NetApp Volumes Unable to create or update AD connection"
  description="Unable to create or update AD connection"
  service="microsoft.storage"
  resource="storage"
  ms.author="b-tonya,b-mayada"
  selfhelptype="Generic"
  supporttopicids="32777926"
  resourcetags=""
  productpesids="16469"
  cloudenvironments="public,mooncake,fairfax,blackforest,usnat,ussec"
  articleid="netappadconnector"
  ownershipid="AzureNetAppFiles" />
# NetApp Volumes Unable to create or update AD connection

Use these recommendations to resolve issues pertaining to Active Directory (AD) connections.

## **Recommended Steps**

1. Note that only one Active Directory connection is allowed in a region.
However if "Map multiple accounts to AD server" feature is used then the AD connection will be visible in all NetApp accounts that are under the same subscription and same region. 
Refer to [Number of Active Directory connections](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-faqs#how-many-active-directory-connections-are-supported) for more details
2. Make sure you are registered for the any [public preview features](https://docs.microsoft.com/azure/azure-netapp-files/whats-new). Refer to [Create an Active Directory connection](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb#create-an-active-directory-connection) for registration and more information.
3. If you are using [LDAP with Extended Group for the volume](https://docs.microsoft.com/azure/azure-netapp-files/configure-ldap-extended-groups) and check if you want to [allow local NFS User with LDAP UI](https://docs.microsoft.com/azure/azure-netapp-files/create-volumes-dual-protocol#allow-local-nfs-users-with-ldap-to-access-a-dual-protocol-volume)
4. Please refer [roubleshoot-ldap-volumes](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-ldap-volumes) if you are getting while creating LDAP Volume

## **Recommended Documents**

- [How to create active directory connections](https://docs.microsoft.com/azure/azure-netapp-files/create-active-directory-connections#create-an-active-directory-connection)
- [Create an SMB volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb)
- [Requirements for Active Directory connections](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb#requirements-for-active-directory-connections)
- [Creating NFS Volumes with LDAP Extended Group](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes) and [ConfiguringLDAP with Extended Group for the volume](https://docs.microsoft.com/azure/azure-netapp-files/configure-ldap-extended-groups)