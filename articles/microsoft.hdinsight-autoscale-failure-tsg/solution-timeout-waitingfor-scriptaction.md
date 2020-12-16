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

It is very likely that the `updateManifest` script action timed out in `UpdateAutoScaleConfigurationWorkflow`, which caused `UpdatingError` in cluster status.

Follow below steps to mitigate this issue:
1. Check if the `updateManifest` script action timed out from **LogEntry** or Ambari UI
2. If step 1 is true, escalate a ticket to control plane PG to set cluster state to Running 
3. Check why `updateManifest` script action timed out from **CAmbariAgentLog**

## **Known Issues**

* [UpdateAutoscaleConfigurationWorkflow causes cluster UpdatingError](https://msdata.visualstudio.com/HDInsight/_workitems/edit/640534)


