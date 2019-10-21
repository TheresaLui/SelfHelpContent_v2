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

**Important Note**: Due to an ongoing issue, NSG Flow Logs are not automatically deleted from Blob storage based on retention policy settings. The retention feature has been [temporarily disabled and users are expected to manually delete flow logs](https://docs.microsoft.com/azure/network-watcher/network-watcher-delete-nsg-flow-log-blobs).

### **I could not enable NSG Flow Logs**

* "Microsoft.Insights" resource provider is not registered

If you received an *AuthorizationFailed* or a *GatewayAuthenticationFailed* error, you might have not enabled the Microsoft Insights resource provider on your subscription. Please [follow the instructions](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal#register-insights-provider) to enable the Microsoft Insights provider.

### **I have enabled NSG Flow Logs but do not see data in my storage account**

* **Setup time**

NSG Flow Logs may take up to 5 minutes to appear in your storage account (if configured correctly). A PT1H.json will appear which can be accessed [as described here](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal#download-flow-log).

* **Service Endpoints exist on your VNet**

NSG Flow Logs does not work on NSGs with [Service endpoints](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoints-overview) enabled. If you had Service Endpoints on your Vnet or have recently added one, NSG Flow Log data will stop being captured.

See [How do I use NSG Flow Logs with Service Endpoints?](https://docs.microsoft.com/azure/network-watcher/frequently-asked-questions#how-do-i-use-nsg-flow-logs-with-service-endpoints) for help.

* **Storage account is behind a firewall**

NSG Flow Logs cannot write to storage accounts behind a firewall. This issue is resolved by allowing "All networks" to access the storage account.

See [How do I disable the firewall on my storage account?](https://docs.microsoft.com/azure/network-watcher/frequently-asked-questions#how-do-i-disable-the--firewall-on-my-storage-account) for help.


* **No Traffic on your NSGs**

Sometimes you will not see logs because your VMs are not active or there are upstream filters at an App Gateway or other devices that are blocking traffic to your NSGs.

### **I want to automate NSG Flow Logs**

Support for automation via ARM templates is currently not available for NSG Flow Logs. This [feature is in development](https://feedback.azure.com/forums/217313-networking/suggestions/37713784-arm-template-support-for-nsg-flow-logs).
