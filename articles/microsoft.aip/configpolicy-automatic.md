<properties
  pagetitle="Azure Information Protection classic client - Creating and configuring Labels and Policies - Automatic classification not behaving as expected&quot;&#xD;"
  description="Azure Information Client - Creating and configuring Labels and Policies - Automatic classification not behaving as expected"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel"
  selfhelptype="Generic"
  supporttopicids="32727936"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="configpolicy_automatic"
  ownershipid="AzureIdentity_InformationProtection" />
# Azure Information Protection classic client - Creating and configuring Labels and Policies - Automatic classification not behaving as expected"

This article is relevant for the Azure Information Protection classic client only. 

To provide a unified and streamlined customer experience, the classic client and label management in the Azure Portal are being deprecated as of March 31, 2021. Learn more in the [official deprecation notice](https://techcommunity.microsoft.com/t5/microsoft-security-and/azure-aip-portal-label-amp-policy-management-admin-experience/ba-p/2182678).

## **Recommended Steps**

1. If you are having issues with automatic labeling, review [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-classification) and [What the sensitive information types look for](https://docs.microsoft.com/office365/securitycompliance/what-the-sensitive-information-types-look-for)<br>

2. Check if you are using scoped policies which aren't configured properly: [How to configure the Azure Information Protection policy for specific users by using scoped policies](https://docs.microsoft.com/azure/information-protection/configure-policy-scope)

3. If automatic labeling isn't working for Outlook when attaching a labeled document, verify that DRMEncryptProperty isn't defined as described here: [IRM registry settings for security](https://docs.microsoft.com/deployoffice/security/protect-sensitive-messages-and-documents-by-using-irm-in-office#office-2016-irm-registry-key-options)

4. If you used the [built-in information types](https://support.office.com/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b) for your Azure Information Protection policy, verify that your content matches the expected format

5. Verify that the label is appropriately configured for **Automatic** or **Recommended**

6. Note that **Automatic** labeling is available for all Office apps, whereas **Recommended** is available for all Office apps except for Outlook

7. You cannot use automatic classification for documents and emails that were previously manually labeled, or previously automatically labeled with a higher classification. More information can be found here: [How automatic or recommended labels are applied](https://docs.microsoft.com/azure/information-protection/configure-policy-classification#how-automatic-or-recommended-labels-are-applied)

8. If you still experiencing issues, collect Azure Information Protection client logs, and attach the exported logs to this ticket.


### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Sensitivity**/**Protect** button > **Help and feedback**
3. Select **Export Logs**
4. Save the logs to a location of your choice and then attach them to this service request.

## **Recommended Documents**

* [How to configure conditions for automatic and recommended classification for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/configure-policy-classification)<br>
* [How-to guides for common scenarios that use Azure Information Protection](https://docs.microsoft.com/azure/information-protection/how-to-guides)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
