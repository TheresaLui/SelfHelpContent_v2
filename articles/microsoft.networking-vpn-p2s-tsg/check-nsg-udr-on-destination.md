<properties
	pageTitle="Guidelines (other OS)"
	description="Guidelines (other OS)"
	service="microsoft.network"
	resource="VirtualNetworkGateway"
	authors="stegag"
	ms.author="stegag"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32584878,32591156"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="a72e15d8-dcb9-43c0-b578-ac3d9398466e"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check if destination is reachable

1. Identify the destination VM in ASC
1. from the **Diagnostics** Tab, select **Test Traffic**
1. Select "TunnelOrLocalIn" as the **Traffic Direction**
1. Insert the IP address of the Point to site client as the **Source**
1. Insert the IP address of the Azure VM as the **Destination**
1. Populate TCP ports according to your scenario
1. Execute the Test Traffic diagnostic by clicking on **Run**
