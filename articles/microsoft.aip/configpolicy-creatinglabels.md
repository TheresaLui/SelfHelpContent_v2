<properties
  pagetitle="Azure Information Protection - Creating and configuring Labels and Policies - Creating Labels&quot;&#xD;"
  description="Azure Information Protection - Creating and configuring Labels and Policies - Creating Labels"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel"
  selfhelptype="Generic"
  supporttopicids="32727941"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="configpolicy_creatinglabels"
  ownershipid="AzureIdentity_InformationProtection" />
# Azure Information Protection - Creating and configuring Labels and Policies - Creating Labels"

To provide a unified and streamlined customer experience, the classic client and label management in the Azure portal are being deprecated as of March 31, 2021. Learn more in our [new article](https://techcommunity.microsoft.com/t5/microsoft-security-and/azure-aip-portal-label-amp-policy-management-admin-experience/ba-p/2182678).

## **Recommended Steps**

1. If you migrated to Azure Information Protection unified labeling and you're having issues using the Microsoft 365 Security and Compliance Center to manage your policies, create a support ticket to the Security and Compliance Center team: [Contact support for business products - Admin Help](https://docs.microsoft.com/microsoft-365/admin/contact-support-for-business-products?view=o365-worldwide&tabs=online).

2. If you recently changed/created the labels and changes are not updated, please wait 24 hours before raising a support ticket.

3. If you require assistance with creating labels in the Azure Information Protection area of the Azure portal, review [Create a new Azure Information Protection label for specific users](https://docs.microsoft.com/azure/information-protection/quickstart-label-specificusers) and [How to create a new label for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-new-label).

4. If you are missing the Sensitivity labels in Excel only and your client appears to work offline, make sure to remove any files in the following folders: 

```
C:\Users\<UserName>\AppData\Roaming\Microsoft\Excel\XLSTART
C:\Program Files\Microsoft Office\Root\Office16\XLSTART 
```

And also add the following Registry key:

```
[HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Common\Security\Labels]
"UseOfficeForLabelling"=dword:00000000
```

### Export Azure Information Protection logs

1. Open an Office document or create a new email message in Outlook
2. Select the **Sensitivity**/**Protect** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to a location of your choice and then attach them to this service request

## **Recommended Documents**

* [Quickstart: Create a new Azure Information Protection label for specific users](https://docs.microsoft.com/azure/information-protection/quickstart-label-specificusers)<br>
* [How to create a new label for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-new-label)<br>
* [Create and Manage Sensitivity Labels](https://support.office.com/article/create-and-manage-sensitivity-labels-2fb96b54-7dd2-4f0c-ac8d-170790d4b8b9)
* [Use sensitivity labels in Office apps](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-office-apps)<br>
* [Configuring the Azure Information Protection policy](https://docs.microsoft.com/azure/information-protection/configure-policy)<br>
* [How-to guides for common scenarios that use Azure Information Protection](https://docs.microsoft.com/azure/information-protection/how-to-guides)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
