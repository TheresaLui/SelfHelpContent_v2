<properties
	pageTitle="TimedOutWaitingForAmbariScriptActionErrorCode"
	description="TimedOutWaitingForAmbariScriptActionErrorCode"
	service="Microsoft.HDInsight"
	resource="Microsoft.HDInsight/clusters"
	authors="Jacky-hdi"
	ms.author="linjzhu"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a82d221b-0873-4120-a195-3edf5fdb468e"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# TimedOutWaitingForAmbariScriptActionErrorCode

<!--issueDescription-->

***INTERNAL CONTENT DO NOT PROVIDE TO CUSTOMER***

<!--/issueDescription-->

It is highly possible updateManifest script action timeout in UpdateAutoScaleConfigurationWorkflow which caused UpdatingError in cluster status.

Please follow below steps to mitigate this issue:
1. check whether updateManifest script action timeout from **LogEntry** or Ambari UI
2. if step 1 is true, please escalate a ticket to control plane PG to set cluster state to Running 
3. check why updateManifest script action timeout from **CAmbariAgentLog**

## **Known Issues**

* [UpdateAutoscaleConfigurationWorkflow cause cluster UpdatingError](https://msdata.visualstudio.com/HDInsight/_workitems/edit/640534)


