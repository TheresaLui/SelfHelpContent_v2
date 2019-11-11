<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster creation failure"
	description="Diagnose and resolve issues with Databricks cluster creation failure"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677678"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="71514fd7-4e3b-4a7e-b213-287efc7fe5b2"
/>

# Diagnose and resolve issues with Databricks cluster creation failure

## **Recommended Steps**

* If you are getting [error for resource quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors) you can increase quota by following these steps:

    * Go to [subscriptions](https://portal.azure.com/#blade/Microsoft_Azure_Billing/SubscriptionsBlade)
    * Select the subscription that needs an increased quota
    * Select Usage + quotas
    * In the upper right corner, select Request increase
    * Fill in the forms for the type of quota you need to increase

* To check current resources, please navigate to: Azure Portal under your subscription --> Usage + quotas


* If clusters are idle for a period of 30 days then they will be automatically deleted. To avoid this, you can pin them which will not allow for the cluster deletion. More information:

	* [Pin a Cluster](https://docs.azuredatabricks.net/clusters/clusters-manage.html#pin-a-cluster)
	* [Delete a Cluster](https://docs.azuredatabricks.net/clusters/clusters-manage.html#cluster-delete)
	
## **Recommended Documents**

* [Cluster Failed to Launch](https://kb.azuredatabricks.net/clusters/cluster-failed-launch.html)

* How to resolve [Error: The subscription is not registered to use namespace 'Microsoft.Compute'](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-register-provider-errors)
