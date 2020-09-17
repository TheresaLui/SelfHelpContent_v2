<properties
	pageTitle="Azure Information Protection - Creating and configuring Labels and Policies - Creating Labels"
	description="Azure Information Protection - Creating and configuring Labels and Policies - Creating Labels"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727941"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="configpolicy_creatinglabels"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection - Creating and configuring Labels and Policies - Creating Labels"

## **Recommended Steps**

1. If you migrated to UL and using SCC to manage your policies, raise a support ticket to Security and Compliance Center team: [Contact support for business products - Admin Help](https://docs.microsoft.com/microsoft-365/admin/contact-support-for-business-products?view=o365-worldwide&tabs=online)

2. If you recently changed/created the labels and changes are not updated, please wait 24 hours before raising a support ticket

3. If you require assistance with creating labels on AIP portal, review [Create a new Azure Information Protection label for specific users](https://docs.microsoft.com/azure/information-protection/quickstart-label-specificusers) and [How to create a new label for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-new-label)

4. If you are missing the Sensitivity labels in Excel only and your client appears to work offline, make sure to remove any files in the following folders: 

```
C:\Users\<UserName>\AppData\Roaming\Microsoft\Excel\XLSTART
C:\Program Files\Microsoft Office\Root\Office16\XLSTART 
```

and add the following Registry key:

```
[HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Common\Security\Labels]
"UseOfficeForLabelling"=dword:00000000
```

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect**/**Sensitivity** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [Quickstart: Create a new Azure Information Protection label for specific users](https://docs.microsoft.com/azure/information-protection/quickstart-label-specificusers)<br>
* [How to create a new label for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-new-label)<br>
* [Create and Manage Sensitivity Labels](https://support.office.com/article/create-and-manage-sensitivity-labels-2fb96b54-7dd2-4f0c-ac8d-170790d4b8b9)
* [Use sensitivity labels in Office apps](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-office-apps)<br>
* [Configuring the Azure Information Protection policy](https://docs.microsoft.com/azure/information-protection/configure-policy)<br>
* [How-to guides for common scenarios that use Azure Information Protection](https://docs.microsoft.com/azure/information-protection/how-to-guides)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
