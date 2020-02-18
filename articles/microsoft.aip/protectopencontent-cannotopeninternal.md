<properties
	pageTitle="Azure Information Protection - Protecting and Opening Content - Cannot open protected content - Internal"
	description="Azure Information Protection - Protecting and Opening Content - Cannot open protected content - Internal"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727938"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax"
	articleId="protectopencontent_cannot_open_internal"
/>

# Azure Information Protection Protection - Protecting and Opening Content - Cannot open protected content - Internal

## **Recommended Steps**

1. Verify that you are signed in with the correct user account that has permissions to open the protected content
2. If you are trying to open files other than Office documents (such as files that have a file name extension of .ppdf, .pjpg, .ppng, .ptxt, or .pfile) use the Azure Information Protection viewer
3. If you are using Office 2010 to open protected content, verify that you have the Azure Information Protection client installed
4. Review the following documentation to verify that you are using a supported file type with a supported application: [Applications that support Azure Rights Management data protection](https://docs.microsoft.com/azure/information-protection/requirements-applications)
5. If you need to open a content where you don't have permissions to (user has left the company, etc.) you can use the Super User feature: [Configuring super users for Azure Information Protection and discovery services or data recovery](https://docs.microsoft.com/azure/information-protection/configure-super-users)
6. Make sure you have followed all network requirements as described at [Firewalls and network infrastructure](https://docs.microsoft.com/azure/information-protection/requirements#firewalls-and-network-infrastructure)
7. If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect**/**Sensitivity** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [How Office applications and services support Azure Rights Management](https://docs.microsoft.com/azure/information-protection/office-apps-services-support)<br>
* [Applications that support Azure Rights Management data protection](https://docs.microsoft.com/azure/information-protection/requirements-applications)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>

