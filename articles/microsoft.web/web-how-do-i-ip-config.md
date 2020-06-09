<properties
	pageTitle="Questions on IP Configuration"
	description="Questions on IP Configuration"
	service="microsoft.web"
	resource="sites"
	authors="sudhat"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32589281"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="c4c47148-71e9-4882-8eed-a6c522f7b4a4"
	ownershipId="Compute_AppService"
/>
# Questions on IP Configuration
## **Recommended documents** 
<b>How to get reserved or dedicated Inbound IP Address for your Web Site?</b> <br>
If  you need to configure a dedicated\reserved IP address for inbound calls made to the azure web app site, you will need to install and configure an IP based SSL certificate.  Please note that in order to do this your App Service Plan should be in Basic or higher pricing tier. <br>
<b>How to find the outbound IP addresses? </b><br>
Please follow the steps listed below:

1. Browse to the details of your specific web app using the new portal at portal.azure.com
2. Towards the top of the details for your web app, there is a link for "All settings". Click the link.
3. Clicking "All settings" will open up a list of web app information that you can drill into further. The specific information to drill into is "Properties". Click on the "Properties" selection.
4. Within the "Properties" UX, there is a textbox showing the set of Outbound IP Addresses. Using the icon to the side of the "Outbound IP Addresses" textbox you can select all of the addresses. Pressing Ctrl+C will then copy the addresses to the clipboard.