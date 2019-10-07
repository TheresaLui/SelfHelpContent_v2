<properties
	pageTitle="Common issues for NSG Flow Logs"
	description="Common issues for NSG Flow Logs"
	infoBubbleText="Common Solutions Template"
	service="microsoft.network"
	resource="networkwatcher"
	authors="damendo"
	ms.author="damendo"
	displayOrder="2"
	articleId="23f8d822-ea47-49a0-8638-95e9d8d1113f"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32606424"
	resourceTags=""
	productPesIds="16160"
	cloudEnvironments="public"
/>

# Common issues with NSG Flow Logs

## **Recommended Steps**

Important Note: Due to an ongoing issue, NSG Flow Logs are not automatically deleted from Blob storage based on retention policy settings. The retention feature has been temporarily disabled and users are expected to manually delete flow logs. [Read more here](https://docs.microsoft.com/azure/network-watcher/network-watcher-delete-nsg-flow-log-blobs).

### **I could not enable NSG Flow Logs**

* "Microsoft.Insights" resource provider is not registered

If you received an *AuthorizationFailed* or a *GatewayAuthenticationFailed* error, you might have not enabled the Microsoft Insights resource provider on your subscription. Please [follow the instructions](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal#register-insights-provider) to enable the Microsoft Insights provider.

### **I have enabled NSG Flow Logs but do not see data in my storage account**

* **Setup time**

NSG Flow Logs may take up to 5 minutes to appear in your storage account (if configured correctly). A PT1H.json will appear which can be accessed [as described here](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal#download-flow-log).

* **Service Endpoints exist on your VNet**

NSG Flow Logs does not work on NSGs with [Service endpoints](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview) enabled. If you had Service Endpoints on your Vnet or have recently added one, NSG Flow Log data will stop being captured.

There are two ways to fix this:

1.  Re-configure NSG flow logs to emit to Azure Storage account without VNET endpoints

* Find subnets with endpoints:

	- On the Azure portal, search for **Resource Groups** in the global search at the top
	- Navigate to the Resource Group containing the NSG you are working with
	- Use the 2nd dropdown to filter by type and select **Virtual Networks**
	- Click on the Virtual Network containing the Service Endpoints
	- Select **Service endpoints** under **Settings** from the left pane
	- Make a note of the subnets where **Microsoft.Storage** is enabled

* Disabling service endpoints:

	- Continuing from above, select **Subnets** under **Settings** from the left pane
	* Click on the subnet containing the Service Endpoints
	- In the **Service endpoints** section, under **Services**, uncheck **Microsoft.Storage**

You can check the storage logs after a few minutes, you should see an updated TimeStamp or a new JSON file created.

* Disable NSG flow logs

If the Microsoft.Storage service endpoints are a must, you will have to disable NSG Flow Logs.

* **Storage account is behind a firewall**

NSG Flow Logs cannot write to storage accounts behind a firewall. This issue is resolved by allowing "All networks" to access the storage account:

* Find the name of the storage account by locating the NSG on the [NSG Flow Logs overview page](https://ms.portal.azure.com/#blade/Microsoft_Azure_Network/NetworkWatcherMenuBlade/flowLogs)
* Navigate to the storage account by typing the storage account's name in the global search on the portal
* Under the **SETTINGS** section, select **Firewalls and virtual networks**
* Select **All networks** and save it. If it is already selected, no change is needed.  
