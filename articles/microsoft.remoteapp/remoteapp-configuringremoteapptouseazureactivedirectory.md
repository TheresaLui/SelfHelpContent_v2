<properties
	pageTitle="infrastructure setup/configuring remoteapp to use azure active directory"
	description="infrastructure setup/configuring remoteapp to use azure active directory"
	service="microsoft.remoteapp"
	resource=""
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32335802"
	resourceTags=""
	productPesIds="15540"
	cloudEnvironments="public"
	articleId="6c17c100-f2fe-4a7f-8305-9a7d8ebc5068"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# infrastructure setup/configuring remoteapp to use azure active directory

## **Recommended steps**
Review the following items to help identify issues.

1. Ensure your image is valid. If you see a message that contains "GoldImageInvalid" as you are waiting for your collection to provision, your image does not meet the requirements.<br>
[Review the image requirements and make sure you are using a valid template image.](https://azure.microsoft.com/documentation/articles/remoteapp-imagereqs/)
2. If you have network security groups defined in your virtual network on the subnet you are using for your collection, ensure that our listed URLs and ports are accessible from within your subnet.<br>
[Review the list of ports and URLs](https://azure.microsoft.com/documentation/articles/remoteapp-ports/)
3. If you are using your own DNS servers, ensure they are accessible from your Azure RemoteApp virtual network subnet.<br>
[Please refer to Name Resolution for VMs and Role Instances to make sure your DNS servers are configured correcly.](https://azure.microsoft.com/documentation/articles/virtual-networks-name-resolution-for-vms-and-role-instances/)

## **Recommended documents**
[Troubleshoot creating Azure RemoteApp hybrid collections](https://azure.microsoft.com/documentation/articles/remoteapp-hybridtrouble/)
