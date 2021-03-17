<properties
	pageTitle="Which authentication method is the customer using?"
	description="Which authentication method is the customer using?"
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
	articleId="7da837a9-98dc-4668-9b48-2fac7b997ceb"
        ownershipId="Centennial_CloudNet_AzureVPNGateway"
/>

# Check the authentication method 


## Recommended Steps

1. Go to ASC > Resource Explorer and select the VPN gateway.
1. Identify the CustomerSubscriptionID, ResourceID and Region
1. From Jarvis Actions open [Get NRP Subscription details](https://jarvis-west.dc.ad.msft.net/?page=actions&acisEndpoint=Public&managementOpen=false&published=true&selectedNodeType=3&extension=NRP&group=NRP%20Subscription%20Operations&operationId=GetNrpSubscriptionDetails&operationName=Get%20NRP%20Subscription%20Details&inputMode=single&actionEndpoint=Production&genevatraceguid=2f5b46cb-30d3-401a-84c5-68adbfecd5ee)
1. Run the command by providing the CustomerSubscriptionID and Region as parameters
1. From the command output, locate the VPN gateway by searching for the ResourceID
1. If a "vpnClientRootCertificates" parameter exists and is not empty -> the authentication method is **Certificates**<br/>
If a "RadiusServerAddress" parameter exists and is not empty -> the authentication method is **RADIUS** <br/>
If an "aadTenant" parameter exists and is not empty -> the authentication method is **Azure AD**
