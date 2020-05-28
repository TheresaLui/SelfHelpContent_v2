<properties
	pageTitle="I can't delete my virtual network"
	description="Troubleshoot issues related to deleting your virtual network"
	service="microsoft.network"
	resource="virtualnetworks"
	authors="anavin"
	ms.author="anavin"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32584253"
	resourceTags=""
	productPesIds="15526"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="61f24fa9-0fc9-44e8-b419-93f4d7cf005a"
	ownershipId="CloudNet_VirtualNetwork"
/>

# I can't delete my virtual network

## **Recommended Steps**

To resolve the most common issues, try one or more of the following methods:

1. Check your [Connected devices](Microsoft_Azure_Network.VirtualNetworkConnectedDevicesBlade) blade of the virtual network. Make sure to delete all the connected devices. If there are any connected devices, deletion of the virtual network will fail.
2. Make sure you have followed all the steps outlined in the [Troubleshooting: Failed to delete a virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet#troubleshooting-guidance) document
3. If you are unable to delete your virtual network due to a resource in failed state within the network, visit [resources.azure.com](https://resources.azure.com/) and navigate to the resource in the failed state. Then click on the Edit button followed by the PUT button for the resource in the failed state. This will remove your resource from being in the failed state.<br>

## **Recommended Documents**

* [Troubleshooting: Failed to delete a virtual network](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-cannot-delete-vnet)<br>
