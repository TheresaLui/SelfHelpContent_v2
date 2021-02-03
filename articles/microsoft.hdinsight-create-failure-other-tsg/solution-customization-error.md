<properties
	pageTitle="CustomizationFailedErrorCode"
	description="CustomizationFailedErrorCode"
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
	articleId="05498fac-5788-42e9-8bbd-73575f30c097"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# CustomizationFailedErrorCode

<!--issueDescription-->

***INTERNAL CONTENT DO NOT PROVIDE TO CUSTOMER***

Review and validate customer case:
1. HdiDeploymentId

<!--/issueDescription-->

To mitigate the issue:
1. additional information about the failure
```kusto
IaasClusterCRUDEvent  
| where (State == "Aborted" or State == "Error") and HdiDeploymentId == "{HdiDeploymentId}"  
| project HdiDeploymentId, ClusterDnsName, CreatedDate, ErrorDate=PreciseTimeStamp 
| join kind=inner LogEntry on ClusterDnsName 
| where PreciseTimeStamp >= CreatedDate and PreciseTimeStamp <= ErrorDate + totimespan(1m) 
| where TraceLevel == "Error" and Class == "CRUDScriptActionActivityExecutor" 
| project PreciseTimeStamp, RoleInstance, Tid, TraceLevel, Class, Details 
```
2. failure information about the failure
```kusto
CAmbariAgentLog  
| where Tenant == "{HdiDeploymentId}" 
| where Message contains "run_customscriptaction" and Message contains " customscriptaction.logger - ERROR - Execution of custom script failed"  
| project ClusterDnsName, PreciseTimeStamp , Host, Message      
| order by PreciseTimeStamp asc 
```
3. Provide the information to the customer to fix the error in custom script action

## **Possible RCA**

* [RServer CustomizationFailedErrorCode](https://supportability.visualstudio.com/AzureHDinsight/_wiki/wikis/AzureHDinsight/349440/RServer-cluster-create-failures-CustomizationFailedErrorCode)

## **Recommended Documents**
* [Troubleshoot script actions](https://docs.microsoft.com/en-us/azure/hdinsight/troubleshoot-script-action#default-storage-account)
* [Customize HDInsight using script actions](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux)
