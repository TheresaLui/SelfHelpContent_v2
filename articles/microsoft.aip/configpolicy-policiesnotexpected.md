<properties
  pagetitle="Azure Information Protection - Creating and configuring Labels and Policies - Policies not behaving as expected&quot;&#xD;"
  description="Azure Information Protection - Creating and configuring Labels and Policies - Policies not behaving as expected"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel"
  selfhelptype="Generic"
  supporttopicids="32727961"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="configpolicy_policiesnotexpected"
  ownershipid="AzureIdentity_InformationProtection" />
# Azure Information Protection - Creating and configuring Labels and Policies - Policies not behaving as expected"

To provide a unified and streamlined customer experience, the classic client and label management in the Azure Portal are being deprecated as of March 31, 2021. Learn more in the [official deprecation notice](https://techcommunity.microsoft.com/t5/microsoft-security-and/announcing-timelines-for-sunsetting-label-management-in-the/ba-p/1226179).

## **Recommended Steps**

1. If you have migrated to Azure Information Protection unified labeling, and are using the Microsoft 365 Security and Compliance Center (SCC) to manage your policies, raise a support ticket to the Security and Compliance Center team to troubleshoot the policy configuration issues: [Contact support for business products - Admin Help](https://docs.microsoft.com/microsoft-365/admin/contact-support-for-business-products?view=o365-worldwide&tabs=online).
2. If you recently changed/created the labels, and the changes are not updated, wait 24 hours before raising a support ticket.
3. **Classic client only**:
     -  If you are having issues with visual markings, review [When visual markings are applied](https://docs.microsoft.com/azure/information-protection/configure-policy-markings#when-visual-markings-are-applied).<br>
     -  If you are having issues with automatic labeling, please review [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-classification) and [What the sensitive information types look for](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for).<br>
     -  Check if you are using scoped policies that aren't configured properly: [How to configure the Azure Information Protection policy for specific users by using scoped policies](https://docs.microsoft.com/azure/information-protection/configure-policy-scope)

4. If you are having issues with Native/Pfile protection, review [File API configuration](https://docs.microsoft.com/azure/information-protection/develop/file-api-configuration).
5. If automatic labeling isn't working for Outlook when attaching a labeled document, or if Label information doesn't appear properly on files using PowerShell or other applications, verify that the `DRMEncryptProperty` isn't defined as described here: [IRM registry settings for security](https://docs.microsoft.com/deployoffice/security/protect-sensitive-messages-and-documents-by-using-irm-in-office#office-2016-irm-registry-key-options)
6. **Unified labeling client only**: If you are encountering issues regarding justification messages or default labels, review [Order of precedence - how conflicting settings are resolved](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide-customizations#order-of-precedence---how-conflicting-settings-are-resolved).
7. If you're missing the Sensitivity labels in Excel only, and your client appears to work offline, make sure to remove any files in the following folders: 

    ```
    C:\Users\<UserName>\AppData\Roaming\Microsoft\Excel\XLSTART
    C:\Program Files\Microsoft Office\Root\Office16\XLSTART 
    ```

    and add the following Registry key:

    ```
    [HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Common\Security\Labels]
    "UseOfficeForLabelling"=dword:00000000
    ```

If you're still experiencing issues after reviewing the preceding steps, collect Azure Information Protection client logs and attach the exported logs to this ticket.

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook.
2. Select the **Protect**/**Sensitivity** button > **Help and feedback**.
3. Select **Export Logs**.
4. Save the logs to a location of your choice, and attach them to this service request.

## **Recommended Documents**

* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>

**Unified labeling client only:**
* [Create and configure sensitivity labels and their policies](https://docs.microsoft.com/microsoft-365/compliance/create-sensitivity-labels)<br>
* [Use sensitivity labels in Office apps](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels-office-apps)<br>
* [Quickstart: Deploy the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/quickstart-deploy-client)<br>


**Classic client only**: 

* [How to configure a label for visual markings for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-markings)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
