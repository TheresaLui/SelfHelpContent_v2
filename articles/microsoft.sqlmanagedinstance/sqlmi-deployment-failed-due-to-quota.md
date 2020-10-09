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
	diagnosticScenario="SqlMISubscriptionLevelInsights"
	selfHelpType="diagnostics"
	supportTopicIds="32637218,32637232,32637269,32674897,32637301,32637315"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLMI"
/>
# We ran diagnostics on your subscription and found an issue

## **Deployment request failed because it would exceed the quota allowance**

<!--issueDescription-->  
We detected that a Managed Instance named **<!--$ManagedInstanceResource-->ManagedInstanceResource<!--/$ManagedInstanceResource-->** in Resource Group **<!--$RGname-->RGname<!--/$RGname-->** failed to deploy around **<!--$eventTimestamp-->eventTimestamp<!--/$eventTimestamp-->**.  

<!--$Message-->Message<!--/$Message-->
<!--/issueDescription-->

## **Recommended Steps**

* Instead of a **Technical** issue type, select **Service and subscription limits (quotas)** for **Issue type** in the previous step
* Use the following steps to request quota increase:

	- Navigate to previous step by clicking on **<< Previous: Basics**
	- For **Issue type**, select **Service and subscription limits (quotas)**
	- For **Subscription**, select the subscription whose quota you want to increase
	- For **Quota type**, select **SQL Database Managed Instance**

* Select **Next: Solutions >>**:

	- In the **Details** window, select **Enter details** to enter additional information

* Click **Provide details** to display the **Quota details** window that enables you to add additional information, with the following steps:

	- In the **Region** list, select the Azure region to target
	- Enter the new limits you are requesting for **Subnet** and **vCore**
	
For more information, see [Overview Azure SQL Database managed instance resource limits](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits).

* Submit your request

The final step is to fill in the remaining details of your SQL Database quota request. Then select **Next: Review + create>>**, and after reviewing the request details, click **Create** to submit the request.

After you submit your request, it will be reviewed. You will be contacted with an answer based on the information you provided in the form.
