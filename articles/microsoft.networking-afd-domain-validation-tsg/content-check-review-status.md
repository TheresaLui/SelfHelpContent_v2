<properties
	pageTitle="How to check the current status of certificateion validation"
	description="How to check the current status of certificateion validation"
	service="Microsoft.Network/"
	resource="Microsoft.Network/frontDoors"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="85628222-2eff-4ed2-a382-89313c52a5a2"
   ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check the current status of certificate validation

1. Go to the URL of the domain in your browser
2. Using F12/Developer Tools, check the X-Azure-Ref response headers
3. Go to [AFD Control Panel](https://www.afdcp.com) and go to Check Impression Log Search Tab
4. Enter the X-Azure-Ref value string and check the output (even if it errors) for the ""Tenant"" GUID
5. Modify the following URL and go to it https://www.afdcp.com/api/v2.0/Tenants/$TENANTGUID$/KeyVaultCertificates
6. JSON response will return with StatusDetails showing the Status and Details
7. Please note the Order ID in the Status Details
