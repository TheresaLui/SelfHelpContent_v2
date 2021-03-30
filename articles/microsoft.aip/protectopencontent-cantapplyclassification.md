<properties
	pageTitle="Azure Information Protection - Protecting and Opening Content - Unable to apply a classification label"
	description="Azure Information Protection - Protecting and Opening Content - Unable to apply a classification label"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727971"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="protectopencontent_cantapplyclassification"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection client - Unable to apply a classification label

## **Recommended Steps**

1. Select **Reset Settings** from the **Sensitivity/Protect** button on the Office ribbon, then **Help and feedback**. 

    This action signs out the user, deletes the currently downloaded Azure Information Protection policy, and resets the user settings for the Azure Rights Management service.
1. Azure Information Protection does not support having multiple versions of Office installed and multiple users signed in to Office. Try again after signing out all users currently signed into Office. [More information](https://docs.microsoft.com/azure/information-protection/requirements#applications)
1. The Azure Information Protection clients do not support multiple versions of Office on the same computer. These clients also do not support switching user accounts in Office.
1. If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket.

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Sensitivity** or **Protect** button -> **Help and feedback**.
3. Select **Export Logs**.
4. Save the logs to a location of your choice and then attach them to this service request.

## **Recommended Documents**

* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quickstart: Deploy the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/quickstart-deploy-client)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
