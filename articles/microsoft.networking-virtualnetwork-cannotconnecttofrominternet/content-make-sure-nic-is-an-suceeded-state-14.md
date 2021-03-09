<properties
	  pageTitle="Make sure Nic is an suceeded state"
	  description="Make sure Nic is an suceeded state"
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
	  articleId="a1204c7b-7441-4d97-ab98-8e095fb67264"
	  ownershipId="Centennial_Cloudnet_virtualNetwork"
/>

# Make sure Nic is an suceeded state

"Make sure that the NIC of the destination VM is in a succeeded state.

## Recommended Steps

1. Open the destination VM in ASC
2. Go to Networking
3. Confirm if the status of the NIC is in a Succeeded state
 *if there is more than one NIC(s) make sure that the NIC holding the Private IP address which the customer is trying to reach is in a Succeded state*
 
If the destination VM is a Windows machine also check if the NIC status is in the OS is OK as well:
1. Open the Diagnostics tab of the VM in ASC
2. Create a Screenshot of the VM
3. The VM screenshot shows that the OS is fully loaded but there's no network (there is a red cross on the NIC)"

