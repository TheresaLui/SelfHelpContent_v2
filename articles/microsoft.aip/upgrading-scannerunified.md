<properties
  pagetitle="Azure Information Protection  - Upgrading and Migration - Upgrade the AIP Unified Labeling Scanner&#xD;"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel,esagmon"
  selfhelptype="Generic"
  supporttopicids="32727977"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="mip_upgrading_scanner_unified"
  ownershipid="AzureIdentity_InformationProtection" />
# Azure Information Protection  - Upgrading and Migration - Upgrade the AIP Unified Labeling Scanner

## **Recommended Steps**

1. Follow the steps at [Upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide#upgrading-the-azure-information-protection-scanner)
2. Run [`Start-AIPScannerDiagnostics`](https://docs.microsoft.com/powershell/module/azureinformationprotection/start-aipscannerdiagnostics) to troubleshoot common issues when deploying the scanner

**Demo**: [Watch our AIP on-premises scanner installation video for standard deployments](https://techcommunity.microsoft.com/t5/microsoft-security-and/mip-scanner-deployment-watch-our-video/ba-p/2023277?attachment-id=32620)

### Export Azure Information Protection Scanner logs

1. In the user directory for the user that is running the scanner service, navigate to `%localappdata%\Microsoft\MSIP`
2. Zip all the contents in the **MSIP** folder
3. Save the logs to your choice of location, and attach them to your service request

**Note**: You can also use [Export-AIPLogs -OnBehalfOf](https://docs.microsoft.com/powershell/module/azureinformationprotection/export-aiplogs) to export your logs via PowerShell.

**Troubleshooting Guide**

Troubleshoot your on-premises scanner deployment with our [Troubleshooting Guide](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-tsg)

## **Recommended Documents**

* [Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)<br>
* [Specify and use the Token parameter for Set-AIPAuthentication](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide-powershell#specify-and-use-the-token-parameter-for-set-aipauthentication)<br>
* [Run a discovery cycle and view reports for the scanner](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-manage)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)