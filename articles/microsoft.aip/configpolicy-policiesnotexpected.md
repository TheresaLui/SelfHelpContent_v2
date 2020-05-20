<properties
	pageTitle="Azure Information Protection - Creating and configuring Labels and Policies - Policies not behaving as expected"
	description="Azure Information Protection - Creating and configuring Labels and Policies - Policies not behaving as expected"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727961"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="configpolicy_policiesnotexpected"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection Protection - Creating and configuring Labels and Policies - Policies not behaving as expected"

## **Recommended Steps**

1. If you are having issues with visual markings, please review [When visual markings are applied](https://docs.microsoft.com/azure/information-protection/configure-policy-markings#when-visual-markings-are-applied)<br>

2. If you are having issues with automatic labeling, please review [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-classification) and [What the sensitive information types look for](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for)<br>

3. If you are having issues with Native/Pfile protection, please review [File API configuration](https://docs.microsoft.com/azure/information-protection/develop/file-api-configuration)

4. Check if you are using scoped policies which aren't configured properly: [How to configure the Azure Information Protection policy for specific users by using scoped policies](https://docs.microsoft.com/azure/information-protection/configure-policy-scope)

5. If automatic labeling isn't working for Outlook when attaching a labeled document, verify that DRMEncryptProperty isn't defined as described here: [IRM registry settings for security](https://docs.microsoft.com/deployoffice/security/protect-sensitive-messages-and-documents-by-using-irm-in-office#office-2016-irm-registry-key-options)

6. If you still experiencing issues, please collect Azure Information Protection client logs and attach the exported logs to this ticket.

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect**/**Sensitivity** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [How to configure a label for visual markings for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-markings)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Use sensitivity labels in Office apps](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-office-apps)<br>
* [Create and configure sensitivity labels and their policies](https://docs.microsoft.com/microsoft-365/compliance/create-sensitivity-labels)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
