<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation failure"
	description="Diagnose and resolve issues with Databricks cluster creation failure"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32730914"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="221c98e1-1bd8-4a79-800d-58bc8ce90b6e"
ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks cluster creation failure

## **Recommended Steps**

### **How To**
* [Use Resource Manager template to create Azure Workspace](https://docs.microsoft.com/azure/azure-databricks/quickstart-create-databricks-workspace-resource-manager-template)
* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/udr.html) to solve this problem.
* [Set Automatic termination](https://docs.microsoft.com/azure/databricks/clusters/clusters-manage#automatic-termination) 

* You can use an Azure Firewall to create a VNet-injected workspace in which all clusters have a single IP outbound address. The single IP address can be used as an additional security layer with other Azure services and applications that allow access based on specific IP addresses: [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://docs.microsoft.com/azure/databricks/kb/cloud/azure-vnet-single-ip)

* If clusters are idle for a period of 30 days then they will be automatically deleted. To avoid this, you can pin them which will not allow for the cluster deletion. More information:

	* [Pin a Cluster](https://docs.azuredatabricks.net/clusters/clusters-manage.html#pin-a-cluster)
	* [Delete a Cluster](https://docs.azuredatabricks.net/clusters/clusters-manage.html#cluster-delete)

### **Troubleshooting**
* [Unexpected Cluster Termination](https://kb.azuredatabricks.net/clusters/termination-reasons.html#unexpected-cluster-termination)
* [Cluster Failed to Launch](https://kb.azuredatabricks.net/clusters/cluster-failed-launch.html)
* [Error: The subscription is not registered to use namespace 'Microsoft.Compute'](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-register-provider-errors)

## **Recommended Documents**
* If you are getting [error for resource quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors) you can increase quota by following these steps:

    * Go to [subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
    * Select the subscription that needs an increased quota
    * Select Usage + quotas
    * In the upper right corner, select Request increase
    * Fill in the forms for the type of quota you need to increase

Note: To check current resources, please navigate to: Azure Portal under your subscription --> Usage + quotas


	



