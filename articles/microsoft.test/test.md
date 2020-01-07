<properties
	pageTitle="Data Explorer - Availability and Connectivity"
	description="Unable to connect"
	ms.author="sischleg"
	authors="simonschlegel"
	selfHelpType="generic"
	productPesIds="16602"
	supportTopicIds="32613503"
	cloudEnvironments="public"
	articleId="de-unable-to-connect-b514fd9e3b832"
/>

# I can't connect to my cluster in Azure Data Explorer

If you're not able to connect to a cluster in Azure Data Explorer, follow these steps.

## **Recommended Steps**
1. Ensure the connection string is correct. It should be in the form: <br>*https://[ClusterName].[Region].kusto.windows.net*
2. Ensure you have adequate permissions. If you don't, you'll get a response of *unauthorized*. For more information about permissions, see [Manage database permissions](https://docs.microsoft.com/azure/data-explorer/manage-database-permissions). If necessary, work with your cluster administrator so they can add you to the appropriate role.
3. Verify that the cluster hasn't been deleted: review the activity log in your subscription.
4. Check the [Azure service health dashboard](https://azure.microsoft.com/status/). Look for the status of Azure Data Explorer in the region where you're trying to connect to a cluster. If the status isn't Good (green check mark), try connecting to the cluster after the status improves.
5. If you still need assistance solving your issue, please continue your support request in the Azure portal.

## **Recommended Documents**

* [Failure to connect to a cluster in Azure Data Explorer](https://docs.microsoft.com/en-us/azure/data-explorer/troubleshoot-connect-cluster)<br>
* [Kusto connection strings](https://docs.microsoft.com/en-us/azure/kusto/api/connection-strings/kusto)<br>
* [Manage database permissions](https://docs.microsoft.com/azure/data-explorer/manage-database-permissions)
