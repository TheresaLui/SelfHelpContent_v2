<properties
	  pageTitle="Reset the NIC of the VM"
	  description="Reset the NIC of the VM"
      service="Microsoft.network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="5ed20b20-3cab-4b60-827f-d5402f515fcd"
	  ownershipId="Centennial_Cloudnet_virtualNetwork"
/>

# Reset the NIC of the VM

Reset the NIC of the VM

## Recommended Steps

1. Ask the customer to reset the NIC of the VM and check if they can connect to it after doing this
2. Check the status of the NIC once again to make sure the state is Succeeded

If the status is succeeded, but the screenshot of the VM still shows the adapter is failed(red cross) after you have asked the customer to reset it, you can collaborate with the Windows Team. If you wish to troubleshoot this yourself refer to the Red-Cross-on-NIC Wiki page linked bellow

## Recommended Documents
1. [ed-Cross-on-NIC Wiki page](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265718/Azure_Virtual-Machine_CantRDPSSH_Basic-Workflow_Isolation-Bucket_Red-Cross-on-NIC-Bucket)

