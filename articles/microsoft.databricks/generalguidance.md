<properties
	pageTitle="Provide general guidance and advisory"
	description="Provide general guidance and advisory"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677654"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1305df1d-4f65-4bc0-afc4-d4825784826a"
	ownershipId="AzureData_AzureDatabricks"
/>

# Provide general guidance and advisory

## **Recommended Steps**

* Search the [Knowledge Base](https://kb.azuredatabricks.net/index.html) for guidance on resolving errors and setup issues 
* If you have a question about how Databricks works, please check how to guides at [Azure Databricks Documentation](https://docs.microsoft.com/azure/databricks/getting-started/training-faq)
* [Azure Databricks Best Practices](https://github.com/Azure/AzureDatabricksBestPractices/)

### **Cluster Creation Issues**

If you are getting [error for resource quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors) you can increase quota by following these steps:

* Go to [subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
* Select the subscription that needs an increased quota
* Select Usage + quotas
* In the upper right corner, select Request increase
* Fill in the forms for the type of quota you need to increase
* If your Azure Databricks workspace is deployed to your own virtual network (VNet), you can use custom routes, also known as user-defined routes (UDR), to ensure that network traffic is routed correctly for your workspace. For example, if you connect the virtual network to your on-premises network, traffic may be routed through the on-premises network and unable to reach the Azure Databricks control plane. Please use [User-defined routes](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/udr.html) to solve this problem.
* [How To: Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
     
### **Notebook Execution Issues**

* [Common Errors in Notebooks](https://kb.databricks.com/notebooks/common-errors-in-notebooks.html)
* [Cannot Run Notebook Commands After Canceling Streaming Cell](https://kb.databricks.com/notebooks/streaming-notebook-stuck.html)

### **Job Failure Issues**

* [Problem: Spark Job Fails with Driver is temporarily unavailable](https://kb.azuredatabricks.net/jobs/driver-unavailable.html)
* [Problem: Job Fails Due to Job Rate Limit](https://kb.azuredatabricks.net/jobs/job-rate-limit.html)
* [Problem: Azure Databricks Job Fails Because Library is Not Installed](https://kb.azuredatabricks.net/jobs/job-fails-no-library.html)
* [Problem: Maximum Execution Context or Notebook Attachment Limit Reached](https://kb.azuredatabricks.net/execution/maximum-execution-context.html)

### **Connectivity Issues**

* [Deploy Azure Databricks in your Azure Virtual Network (VNet Injection)](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/vnet-inject)
* [Connect your Azure Databricks Workspace to your On-Premises Network](https://docs.microsoft.com/azure/databricks/administration-guide/cloud-configurations/azure/on-prem-network)
