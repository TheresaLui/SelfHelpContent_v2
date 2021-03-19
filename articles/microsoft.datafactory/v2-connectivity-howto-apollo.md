<properties
  pagetitle="How to"
  service="microsoft.datafactory"
  resource="datafactories"
  ms.author="shelfeng,brianwan"
  selfhelptype="Apollo"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  disableclouds=""
  articleid="v2-connectivity-howto-apollo"
  ownershipid="AzureData_DataFactory"
  supportTopicIds="24f37f63-6f1d-3604-2d20-8743d6187130"
/>

# How to

## How to (need title here)

<<Please add a summary of the issue and how should the customer consume the solutions provided below?>>

### Recommended steps

1. First, find the error returned when you are trying to execute the pipeline or when you are trying to connect to the dataset. Try testing the connection by editing the linked service and selecting **Test connection**. If you are using a self-hosted IR, you can find detailed information in Integration Runtime logs inside the Windows event logs. To find them, go to **Event Viewer** > **Application and Services Logs** > **Integration Runtime** and **Connectors**. 

2. Review the documented errors and solutions.  The following troubleshooting guides provide many common errors and solutions: 

   - If you get any unexpected connectivity errors from Activity, see [Activity troubleshooting guidance](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide) 

   - If you get any unexpected connectivity errors from connectors, see [connector troubleshooting guide](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide)

   - If you get any unexpected connectivity errors from Managed VNet and private links, see [security and access control troubleshooting guide](https://docs.microsoft.com/azure/data-factory/security-and-access-control-troubleshoot-guide) 

   - If you get any unexpected connectivity errors from Self-Hosted IR, see [self-hosted Integration runtime troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide) 

3. If you are using a self-hosted IR to connect to your data, make sure you test your connectivity from the Self-Hosted IR machine, access the **Microsoft Integration Runtime Configuration Manager**, and confirm that it is connected to the cloud service. Then go to the **Diagnostics** tab and test the connection to your data source/sink. You can find detailed information in Integration Runtime logs in Windows event logs. To find them, go to **Event Viewer** > **Application and Services Logs** > **Integration Runtime** and **Connectors**, and then go to step 2. 

4. Make sure that networking security components such as firewalls, Network Security Groups, and VPN configurations have not changed. If your scenario uses any of these components, review the [data movement security considerations](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#firewall-configurations-and-allow-list-setting-up-for-ip-address-of-gateway) documentation to ensure all configurations are correct.  

5. Make sure that ports are on the allow list for both central _corporate_ firewall and local machine _Windows_ firewall. For more details, see [Firewall Whitelisting](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#ports-and-firewalls). 

If your IR uses proxy server, see [Proxy Server](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#proxy-server-considerations).

6. After reviewing the logs and relevant documentation, if you still need assistance, open a support request. Make sure to specify the errors you are addressing and attach the logs that you gathered while troubleshooting the issue. 

<br>

### Recommended documents

- [Activity troubleshooting guidance](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide) 
- [Connector troubleshooting guide](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide). 
- [Security and access control troubleshooting guide](https://docs.microsoft.com/azure/data-factory/security-and-access-control-troubleshoot-guide) 
- [The Integration Runtime Registration Error](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide) 
- [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions) 
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)

<br>

### More resources

Here are additional relevant articles from the web
<azureKB>
    <client>Portal</client>
</azureKB>
