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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="CloudNet_NetAnalytics"
/>

# Common issues with NSG Flow Logs 

## **Recommended Steps**

### **I could not enable NSG Flow Logs**

* "Microsoft.Insights" resource provider is not registered

If you received an *AuthorizationFailed* or a *GatewayAuthenticationFailed* error, you might have not enabled the Microsoft Insights resource provider on your subscription. Please [follow the instructions](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal#register-insights-provider) to enable the Microsoft Insights provider.

### **I have enabled NSG Flow Logs but do not see data in my storage account**

* **Setup time**

NSG Flow Logs may take up to 5 minutes to appear in your storage account (if configured correctly). A PT1H.json will appear which can be accessed [as described here](https://docs.microsoft.com/azure/network-watcher/network-watcher-nsg-flow-logging-portal#download-flow-log).

* **No Traffic on your NSGs**

Sometimes you will not see logs because your VMs are not active or there are upstream filters at an App Gateway or other devices that are blocking traffic to your NSGs.

### **I want to automate NSG Flow Logs**

Support for deployment automation via ARM templates is now available for NSG Flow Logs. Read the [feature announcement](https://azure.microsoft.com/updates/arm-template-support-for-nsg-flow-logs/) for more information. 
