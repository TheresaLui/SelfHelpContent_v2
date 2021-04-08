<properties
  pagetitle="Azure Information Protection - Protecting and Opening Content - Questions about applying protection with the AIP Scanner"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel"
  selfhelptype="Generic"
  supporttopicids="32727962"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="protectopencontent_scannerprotect"
  ownershipid="AzureIdentity_InformationProtection" />
# Azure Information Protection - Protecting and Opening Content - Questions about applying protection with the AIP Scanner

To provide a unified and streamlined customer experience, the classic client and label management in the Azure portal are being deprecated as of March 31, 2021. Learn more from our [new article](https://techcommunity.microsoft.com/t5/microsoft-security-and/azure-aip-portal-label-amp-policy-management-admin-experience/ba-p/2182678).

## **Recommended Steps**

* If you're running the scanner installed with the unified labeling client, run [Start-AIPScannerDiagnostics](https://docs.microsoft.com/powershell/module/azureinformationprotection/start-aipscannerdiagnostics?view=azureipps) to troubleshoot common deployment issues. 
Using this command generates logs that can be uploaded to your case details if you need to proceed with creating a support ticket.

* Troubleshoot your on-premises scanner deployment with our [Troubleshooting Guide](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-tsg)

**Note:** If you're not currently logged in as the user running the scanner service, use the [`Export-AIPLogs -OnBehalfOf`](https://docs.microsoft.com/powershell/module/azureinformationprotection/export-aiplogs?view=azureipps) cmdlet to export logs.

## **Recommended Documents**

* [Configure the scanner to apply classification and protection](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-configure-install#configure-the-scanner-to-apply-classification-and-protection)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [How Office applications and services support Azure Rights Management](https://docs.microsoft.com/azure/information-protection/office-apps-services-support)<br>
* [Applications that support Azure Rights Management data protection](https://docs.microsoft.com/azure/information-protection/requirements-applications)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>

## **Recommended Documents for Scanner DLP**

* [Learn about the Microsoft 365 data loss prevention on-premises scanner](https://docs.microsoft.com/microsoft-365/compliance/dlp-on-premises-scanner-learn?view=o365-worldwide)<br>
* [Get started with the data loss prevention on-premises scanner](https://docs.microsoft.com/microsoft-365/compliance/dlp-on-premises-scanner-get-started?view=o365-worldwide)<br>
* [Use the Microsoft 365 data loss prevention on-premises scanner](https://docs.microsoft.com/microsoft-365/compliance/dlp-on-premises-scanner-use?view=o365-worldwide)<br>