<properties
  pagetitle="Common NetApp Volumes Issues with Create and Delete&#xD;"
  service="microsoft.netapp"
  resource="netappaccounts"
  ms.author="b-kelamb,b-nisood"
  selfhelptype="Generic"
  supporttopicids="32740756"
  resourcetags=""
  productpesids="16469"
  cloudenvironments="public,mooncake,fairfax,blackforest,usnat,ussec"
  articleid="netappvolumesissuecreatedelete"
  ownershipid="AzureNetAppFiles" />
# Common NetApp Volumes Issues with Create and Delete

## Problems Creating or Deleting a Volume

1. If you are creating or deleting volumes using the Azure NetApp Files REST API, you may be issuing requests too quickly and the process is being throttled. Refer to [Throttling Resource Manager Requests](https://docs.microsoft.com/azure/azure-resource-manager/management/request-limits-and-throttling#resource-provider-limits) for limit definitions.
2. If you are having issues deleting a Volume, make sure you have deleted all snapshots that have been created from that volume

## **Recommended Documents**

- [Resource Limits for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-resource-limits)<br>
- [Delegate a subnet to Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-delegate-subnet)<br>
- [Create an SMB volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb)<br>
- [Create an NFS volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes)<br>
- [Getting access to Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-netapp-account)<br>
- [Quickstart: Set up Azure NetApp Files and create an NFS Volumes](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-quickstart-set-up-account-create-volumes)<br>
