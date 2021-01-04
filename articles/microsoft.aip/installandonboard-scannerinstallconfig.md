<properties
  pagetitle="Azure Information Protection (AIP) Scanner - Installing, configuring, and decommissioning&#xD;"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel,esagmon"
  selfhelptype="Generic"
  supporttopicids="32727933"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="mip_onboard_scanner_install_config"
  ownershipid="AzureIdentity_InformationProtection" />
# Azure Information Protection (AIP) Scanner - Installing, configuring, and decommissioning

Most customers can resolve their issues when installing or upgrading the Azure Information Protection (AIP) Scanner by using the following steps. 

## **Recommended Steps**

1. Review the instructions (choose one of the following):
    -  For upgrades (versus for first-time installions), review [upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide#upgrading-the-azure-information-protection-scanner). 

    - For classic client upgrades, review [upgrading the Azure Information Protection scanner](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide#upgrading-the-azure-information-protection-scanner).

    -  For standard deployments, [watch this video: *Installing the AIP on-premises scanner* (7:41)](https://techcommunity.microsoft.com/t5/microsoft-security-and/mip-scanner-deployment-watch-our-video/ba-p/2023277?attachment-id=32620)
    
1. Verify that you comply with all [firewalls and network infrastructure settings requirements](https://docs.microsoft.com/azure/information-protection/requirements#firewalls-and-network-infrastructure).

1. Set policies appropriately:
    - Use the automatic labeling, or include a default label in the policy. For information about sensitivity labels, see the [Microsoft 365 documentation](https://docs.microsoft.com/microsoft-365/compliance/sensitivity-labels?view=o365-worldwide). 

    - If you're upgrading the classic client, follow these guidelines to [configure the Azure Information Protection policy](https://docs.microsoft.com/azure/information-protection/configure-policy). 
    
1. Configure label/protection for relevant file types:

   -  Review [file types supported by the Azure Information Protection unified labeling client](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide-file-types#supported-file-types-for-classification-and-protection). 

   -  If you are working in the [classic client](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide-file-types), and want to change the default behavior, follow these steps to [change the default protection level of files](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide-file-types#changing-the-default-protection-level-of-files).
    
1. Verify that the user account configured to run the scanner service has permissions to access all the configured repositories.

1. If you are using the unified labeling client, run [Start-AIPScannerDiagnostics](https://docs.microsoft.com/powershell/module/azureinformationprotection/start-aipscannerdiagnostics?view=azureipps) to troubleshoot common issues when deploying the scanner. 

1. Review the [Troubleshooting Guide for on-premises scanner deployment](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner-tsg)

1. If you experience issues after completing these steps, export the scanner logs and add them to your support ticket.



### Export AIP scanner logs

1. Go to **%localappdata%\Microsoft\MSIP** under the user context running the scanner service.
2. Zip the entire contents under the **MSIP** folder.
3. Save the logs to your choice of location, and attach them to your service request.

**Note:** You can also export your logs via PowerShell. See [Export-AIPLogs -OnBehalfOf](https://docs.microsoft.com/powershell/module/azureinformationprotection/export-aiplogs).


## **Recommended Documents**

* [Deploy the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)<br>
* [Specify and use the Token parameter for Set-AIPAuthentication](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-powershell#specify-and-use-the-token-parameter-for-set-aipauthentication)<br>
* [Run a discovery cycle and view reports for the scanner](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner#run-a-discovery-cycle-and-view-reports-for-the-scanner)<br>
* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)
