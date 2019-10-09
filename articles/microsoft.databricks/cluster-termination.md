<properties
	pageTitle="Diagnose and resolve issues with Databricks cluster termination"
	description="Diagnose and resolve issues with Databricks cluster termination"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677671"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="b693e759-430f-4b6b-b47d-cfc21029d2aa"
/>

# Diagnose and resolve issues with Databricks cluster termination

## **Recommended Steps**

* By design, clusters which are idle for 30 days will be automatically deleted. To avoid this, you can pin them which will not allow the cluster deletion. More information:

    * [Pin a Cluster](https://docs.azuredatabricks.net/user-guide/clusters/pin.html#pin-a-cluster)
    * [Delete a cluster](https://docs.azuredatabricks.net/user-guide/clusters/delete.html)
    
* For details on who deleted the cluster, please check [cluster event log](https://docs.databricks.com/user-guide/clusters/event-log.html#cluster-event-log)

## **Recommended Documents**

* [Unexpected Cluster Termination](https://kb.azuredatabricks.net/clusters/termination-reasons.html#unexpected-cluster-termination)


