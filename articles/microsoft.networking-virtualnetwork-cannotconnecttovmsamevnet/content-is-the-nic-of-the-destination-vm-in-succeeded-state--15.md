<properties
	  pageTitle="Is the NIC of the destination VM in succeeded state?"
	  description="Is the NIC of the destination VM in succeeded state?"
      service="Microsoft.Network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="1a9b41e2-4f09-42ca-9740-452cb83129eb"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Is the NIC of the destination VM in succeeded state?

Make sure that the NIC of the destination VM is in a succeeded state.

## Recommended Steps

1. Open the destination VM in ASC
2. Go to Networking
3. Confirm if the status of the NIC is in a succeeded state
**Note:** If there is more than one NIC(s), make sure that the NIC holding the Private IP address that the customer is trying to reach is in a succeeded state
 
If the destination VM is a Windows machine, also check if the NIC status is in the OS is good:
1. Open the Diagnostics tab of the VM in ASC
2. Create a screenshot of the VM
3. The VM screenshot shows that the OS is fully loaded, but there's no network (there is a red cross on the NIC)

