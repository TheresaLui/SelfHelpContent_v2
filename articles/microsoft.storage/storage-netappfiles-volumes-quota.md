<properties
  pagetitle="NetApp Volumes Issue with volume quota or size&#xD;"
  description="Issue with volume quota"
  service="microsoft.storage"
  resource="storage"
  ms.author="b-kiudup,b-tonya"
  selfhelptype="Generic"
  supporttopicids="32784417"
  resourcetags=""
  productpesids="16469"
  cloudenvironments="public,mooncake,fairfax,blackforest,usnat,ussec"
  articleid="netappvolumesissuevolumequota"
  ownershipid="AzureNetAppFiles" />
# NetApp Volumes Issue with volume quota or size

Review the following steps to determine the cause of your NetApp Volumes issue.  

## **Recommended Steps**

1. Any consumed snapshot size counts towards the provisioned space of the volume.
2. The volume doesn't automatically grow when it is completely filled. You must either resize the volume, or delete data or snapshots, to create more space.

## **Recommended Documents**

- [Create an NFS volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes)<br>
- [Cost model for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-cost-model)<br>
- [Understanding resource limits for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-resource-limits)<br>
- [How to submit a support request to increase the resource limits that are adjustable for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-resource-limits#request-limit-increase-)<br>
