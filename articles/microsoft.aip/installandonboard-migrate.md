<properties
	pageTitle="Azure Information Protection - Installing, Onboarding, or Decommissioning - Migration from AIP to Unified Labeling - SCC"
	description="Azure Information Protection - Installing, Onboarding, or Decommissioning - Migration from AIP to Unified Labeling - SCC"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727950"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="MIP_Onboard_Install_migrate_to_scc"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection  - Installing, Onboarding, or Decommissioning - Migration from AIP to Unified Labeling - SCC

To provide a unified and streamlined customer experience, the classic client and label management in the Azure Portal are being deprecated as of March 31, 2021. Learn more in the [official deprecation notice](https://aka.ms/aipclassicsunset).


**Note:** If you have already migrated to Azure Information Protection unified labeling, and are using the Microsoft 365 Security and Compliance Center (SCC) to manage your policies, raise a support ticket to the Security and Compliance Center team: [Contact support for business products - Admin Help](https://docs.microsoft.com/microsoft-365/admin/contact-support-for-business-products?view=o365-worldwide&tabs=online)

## Activate protection from the Azure portal

1. If you haven't already done so, open a new browser window and [sign in to the Azure portal](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-policy#signing-in-to-the-azure-portal). 

    Navigate to the **Azure Information Protection** blade. For example, on the hub menu, click **All services** and start typing **Information** in the Filter box. 

    Select **Azure Information Protection**. If you haven't accessed the Azure Information Protection blade before, see the one-time [additional steps](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-policy#to-access-the-azure-information-protection-blade-for-the-first-time) to add this blade to the portal. 

    To open the Azure Information Protection blade, you must have either an [Azure Information Protection Premium plan](https://www.microsoft.com/cloud-platform/azure-information-protection-pricing) or an [Office 365 plan that includes Rights Management](http://download.microsoft.com/download/E/C/F/ECF42E71-4EC0-48FF-AA00-577AC14D5B5C/Azure_Information_Protection_licensing_datasheet_EN-US.pdf). 

    If you have one of these subscriptions but see a message that a valid subscription cannot be found, [contact Microsoft Support](https://docs.microsoft.com/azure/information-protection/get-started/information-support#to-contact-microsoft-support) or use your standard support channels.

1. Locate the **MANAGE** menu options, and select **Protection activation**. Click **Activate**, and then confirm your action. When activation is complete, the information bar displays **Activation finished successfully**.

### Migrate Azure Information Protection labels to Office 365 Security & Compliance Center

1. Make sure you are logged in as a user with **Global Administrator** permissions.
2. Navigate to the **Azure Information Protection** blade.
3. From the **Manage** menu option, select **Unified labeling**.
4. On the **Azure Information Protection - Unified labeling** blade, select **Activate** and follow the online instructions.

Verify that you have the appropriate permissions before activating the Security & Compliance Center Migration:

- [Do you need to be a global admin to configure Azure Information Protection, or can I delegate to other administrators?](https://docs.microsoft.com/azure/information-protection/faqs#do-you-need-to-be-a-global-admin-to-configure-azure-information-protection-or-can-i-delegate-to-other-administrators)<br>
- [Important information about administrative roles after migrating to Security & Compliance Center](https://docs.microsoft.com/azure/information-protection/configure-policy-migrate-labels#important-information-about-administrative-roles)<br>

## **Recommended Documents**

* [How-to guides for common scenarios that use Azure Information Protection](https://docs.microsoft.com/azure/information-protection/how-to-guides)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [How to migrate Azure Information Protection labels to the Office 365 Security & Compliance Center](https://docs.microsoft.com/azure/information-protection/configure-policy-migrate-labels)<br>
* [Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quickstart: Deploy the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/quickstart-deploy-client)<br>
* [How to activate Azure Rights Management from the Azure portal](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-azure)

