<properties
	pageTitle="Access customer workspace and check the issue"
	description="Access customer workspace and check the issue"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1a4e903c-85ff-42da-b7d9-334c998ec274"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Access customer workspace and check the issue

**What is Genie?**

Genie tool is an application that with customer permission allows CSS to access:

1.	Customers workspace
2.	Databricks clusters event logs 
3.	Customers spark logs

Check in the case that the **DatabricksConsent**  is **True**. This gives Microsoft and Databricks permissions to access customers workspace and logs.

**Important**: If DatabricksConsent is False, please get customer written or verbal consent before accessing Genie.

**Create Genie access ticket**

1. Go to Salesforce portal to submit ticket: [Submit Request](https://help.databricks.com/s/submitrequest)
2. Fill all required details making sure to have the following:

    ```
    Business Impact - Low 
    Component - Genie access request
    Check the permission to access Databricks instance
    Workspace ID
    Cluster ID
    Requestor Organization
    Requestor Subscription ID
    Requestor Ticket ID
    ```

3. Submit request and copy ticket number to use it afterwards

**Access customer workspace**

1. Go to [Genie](https://genie-azure-prod.dev.databricks.com/)
2. Fill customer workspace and ticket details gathered in previous steps
