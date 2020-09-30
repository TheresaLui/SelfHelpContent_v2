<properties
	pageTitle="The deployment request failed because it would exceed the quota allowance for your subscription"
	description="The deployment request failed because it would exceed the quota allowance for your subscription"
	infoBubbleText="The deployment request failed because it would exceed the quota allowance for your subscription"
	service="microsoft.sql"
	resource="managedInstances"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sqlmi-deployment-failed-due-to-quota"
	diagnosticScenario="sqlmideploymentfailedduetoquota"
	selfHelpType="diagnostics"
	supportTopicIds="32637218,32637232,32637269,32674897,32637301,32637315"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI"
/>
# We ran diagnostics on your subscription and found an issue

<!--issueDescription-->  
We detected that a Managed Instance named **{ManagedInstanceResource}** in Resource Group **{RGname}** failed to deploy around **{eventTimestamp}**.  

**{Message}**
<!--/issueDescription-->

## **Recommended Steps**

* Instead of a **Technical** issue type, please select **Service and subscription limits (quotas)** for **Issue type** in the previous step
* Use the following steps to request quota increase:

	1. Navigate to previous step by clicking on **<< Previous: Basics**
	1. For **Issue type**, select **Service and subscription limits (quotas)**
	1. For **Subscription**, select the subscription whose quota you want to increase
	1. For **Quota type**, select **SQL Database Managed Instance**

* Select **Next: Solutions >>**:

	1. In the **Details** window, select **Enter details** to enter additional information

* Clicking **Provide details** displays the **Quota details** window that allows you to add additional information, use the following steps:

	1. In the **Region** list, select the Azure region to target
	1. Enter the new limits you are requesting for **Subnet** and **vCore**
	
For more information, see [Overview Azure SQL Database managed instance resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits).

### Submit your request

The final step is to fill in the remaining details of your SQL Database quota request. Then select **Next: Review + create>>**, and after reviewing the request details, click **Create** to submit the request.

### Next steps

After you submit your request, it will be reviewed. You will be contacted with an answer based on the information you provided in the form.
