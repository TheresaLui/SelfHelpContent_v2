<properties
	pageTitle="Check using RADIUS"
	description="Check using RADIUS"
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
	articleId="f997dc32-a4c1-4b79-b50e-858b36e3443e"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check if the customer is using RADIUS

## Recommended Steps

1. Go to ASC > Resource Explorer and select the VPN gateway.
2. Identify the CustomerSubscriptionID, ResourceID and Region
3. From Jarvis Actions open [Get NRP Subscription details](https://jarvis-west.dc.ad.msft.net/?page=actions&acisEndpoint=Public&managementOpen=false&published=true&selectedNodeType=3&extension=NRP&group=NRP%20Subscription%20Operations&operationId=GetNrpSubscriptionDetails&operationName=Get%20NRP%20Subscription%20Details&inputMode=single&actionEndpoint=Production&genevatraceguid=2f5b46cb-30d3-401a-84c5-68adbfecd5ee)
4. Run the command by providing the CustomerSubscriptionID and Region as parameters
5. From the command output, locate the VPN gateway by searching for the ResourceID
6. If a "vpnClientRootCertificates" parameter exists and is not empty -> the authentication method is **Certificates**<br/>
   1. If a "RadiusServerAddress" parameter exists and is not empty -> the authentication method is **RADIUS** <br/>
   2. If an "aadTenant" parameter exists and is not empty -> the authentication method is **Azure AD**
