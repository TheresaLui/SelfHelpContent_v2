<properties
	pageTitle="Azure NetApp Files volume hit threshold"
	description="Azure NetApp Files volume hit threshold"
	infoBubbleText="We have detected a threshold issue to your Azure NetApp Files volume."
	service="microsoft.storage"
	resource="storage"
	authors="ram-kakani, v-fikhuz"
	ms.author="ramakk, v-fikhuz"
	articleId="NetAppFilesHitThreshold"
	selfHelpType="diagnostics"
	supportTopicIds="32640618"
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# NetApp Files Hit Threshold

## **The number of IPs in use in a VNET with Azure NetApp Files (including peered VNETs) hit threshold**

<!--issueDescription-->
We have identified that your volume <!--$volumename-->[volumename]<!--/$volumename--> may be currently inaccessible from some of your source VMs due to an IP limitation (<1000 IPs in a VNET and peered VNETs) that we have documented under the constraints section of the Azure NetApp Files service network planning public documentation. In order to mitigate the issue, create the Azure NetApp Files volumes in a VNET in itself or a VNET with <1000 IPs and peer it with VNETs which needs direct access to the volume. In case a limit increase is absolutely required, you can as well reach our technical support team via a ticket with your use case, topology and limit required so that we can assess the need and increase the limit as required.

We sincerely apologize for the inconvenience caused. We are working towards improving the platform to meet our customer scale demands in the near future.
<!--/issueDescription-->

## **Recommended Documents**

* [Azure NetApp Files constraints](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-network-topologies#constraints)