<properties
  pagetitle="Azure Information Protection - Configuring the Service - AIP Scanner Classic&#xD;"
  description="Azure Information Protection - Configuring the Service - AIP Scanner Classic"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel"
  selfhelptype="Generic"
  supporttopicids="32727934"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="configservice_scanner_classic"
  ownershipid="AzureIdentity_InformationProtection" />
# Azure Information Protection - Configuring the Service - AIP Scanner Classic

This article is relevant for the Azure Information Protection classic client only. 

To provide a unified and streamlined customer experience, the classic client and label management in the Azure Portal are being deprecated as of March 31, 2021. Learn more in our [new article](https://techcommunity.microsoft.com/t5/microsoft-security-and/azure-aip-portal-label-amp-policy-management-admin-experience/ba-p/2182678).

## **Recommended Steps**

1. If you used the [built-in information types](https://support.office.com/article/What-the-sensitive-information-types-look-for-fd505979-76be-4d9f-b459-abef3fc9e86b) for your Azure Information Protection policy, verify that your content matches the expected format
2. Verify that the label is appropriately configured for **Automatic** or **Recommended**
3. Note that **Automatic** labeling is available for all Office apps, whereas **Recommended** is available for all Office apps except for Outlook
4. Verify that the user account configured to run the scanner service has permissions to access all the configured repositories

If you are still experiencing the issue, collect Azure Information Protection scanner logs and attach the logs to this ticket.


### Export Azure Information Protection Scanner logs

1. Navigate to `%localappdata%\Microsoft\MSIP` under the user context running the scanner service
2. Zip all the contents under the **MSIP** folder.
3. Save the logs to your choice of location, and attach them to your service request

## **Recommended Documents**

* [Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)<br>
* [Specify and use the Token parameter for Set-AIPAuthentication](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-powershell#specify-and-use-the-token-parameter-for-set-aipauthentication)<br>
* [Run a discovery cycle and view reports for the scanner](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-classic#run-a-discovery-cycle-and-view-reports-for-the-scanner)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)