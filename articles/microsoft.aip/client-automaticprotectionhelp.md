<properties
	pageTitle="Azure Information Client - Automatic protection"
	description="Azure Information Client - Automatic protection"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	ms.author="nihendle, orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584330"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
	articleId="e814fd5d-9e33-43dc-871b-7cb3c3c952a8"
/>

# Azure Information Protection client - automatic protection

## **Recommended Steps**

1. If you used the [built-in information types](https://support.office.com/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b) for your Azure Information Protection policy, verify that your content matches the expected format
2. Verify that the label is appropriately configured for **Automatic** or **Recommended**
3. Note that **Automatic** labeling is available for all Office apps, whereas **Recommended** is available for all Office apps except for Outlook
4. If automatic labeling isn't working for Outlook when attaching a labeled document, verify that DRMEncryptProperty isn't defined as described here: [IRM registry settings for security](https://docs.microsoft.com/deployoffice/security/protect-sensitive-messages-and-documents-by-using-irm-in-office#office-2016-irm-registry-key-options)

If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket.

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [How-to guides for common scenarios that use Azure Information Protection](https://docs.microsoft.com/azure/information-protection/how-to-guides)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
