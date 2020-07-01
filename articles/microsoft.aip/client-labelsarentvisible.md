<properties
	pageTitle="Azure Information Client - Labels aren't visible"
	description="Azure Information Client - Labels aren't visible"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	ms.author="nihendle, orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584353"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="f480647e-f515-4015-ad7d-00796bd773a8"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection client - labels aren't visible

## **Recommended Steps**

If your issue is with a label that applies protection, verify the following:

1. You are using an [edition of Office that supports protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements#applications), such as Office 365 ProPlus
2. You are signed in with the correct Azure AD user for your tenant

   * To check your signed-in account, select the **Protect** button -> **Help and Feedback**, and view user account that's displayed

3. If the label is visible in some Office apps but not all Office apps, check whether the label is configured for the **Set user-defined permissions** option:

	* If this option is enabled and **In Outlook apply Do Not Forward** is selected, the label displays in Outlook only
	* If this option is enabled and **In Word, Excel, PowerPoint and File Explorer prompt user for custom permissions** is selected, the label displays in Word, Excel, PowerPoint and File Explorer, but not Outlook

4. Make sure the labels are added to a policy: [Add or remove a label to or from an Azure Information Protection policy](https://docs.microsoft.com/azure/information-protection/configure-policy-add-remove-label)

5. Check if you are using scoped policies which aren't configured properly: [How to configure the Azure Information Protection policy for specific users by using scoped policies](https://docs.microsoft.com/azure/information-protection/configure-policy-scope)

6. If you are experiencing issues with visual markings not being applied, please review the below documents:

	* [How to configure a label for visual markings for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-markings) 
	* [When visual markings are applied](https://docs.microsoft.com/azure/information-protection/configure-policy-markings#when-visual-markings-are-applied)

7. Azure Information Protection does not support having multiple version of Office installed and multiple users signed in to Office. Try to logout all users logged into Office and try again [More information](https://docs.microsoft.com/azure/information-protection/requirements#applications)

8. Make sure you are using the correct client for your deployment. More information can be found [here](https://docs.microsoft.com/azure/information-protection/configure-policy-migrate-labels)

9. If you are using Azure Information Protection Unified Labeling Client, make sure you have published the labels and policies to the relevant users: [How to get started](https://docs.microsoft.com/office365/securitycompliance/sensitivity-labels#how-to-get-started)

10. If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Overview of sensitivity labels](https://docs.microsoft.com/office365/securitycompliance/sensitivity-labels)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
