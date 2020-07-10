<properties
    pageTitle="HDInsight failure due to yarn application have high disk usage"
    description="HDInsight failure due to yarn application have high disk usage"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="143"
    articleId="Hdi_Health_Yarn"
    diagnosticScenario="HDInsightYarnHighDiskUsageInsight"
    selfHelpType="rca"
    supportTopicIds="32636488"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
We determined that the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has high disk usage because of yarn applications running on the affected nodes.
<!--/issueDescription-->
### **Affected Resources**

<!--$Details-->[Details]<!--/$Details-->

## **Recommended Steps**

1. Ensure that yarn.log-aggregation-enabled is enabled. If disabled, NMs will keep the logs locally and not aggregate them in remote store on application completion/termination.
2. Cache also uses disk space, so check if `yarn.nodemanager.localizer.cache.cleanup.interval-ms` (default 10 mins) and `yarn.nodemanager.localizer.cache.target-size-mb` (default 10240 MB) are set to reasonable values
3. Ensure that the cluster size is appropriate for the workload. If the cluster is not appropriately sized, scale up the cluster and retry.
4. `/mnt/resource` might also get filled with orphaned files (as in the case of RM restart). Manually cleaning up `/mnt/resource/hadoop/yarn/log` and `/mnt/resource/hadoop/yarn/local` on the worker nodes would help in this scenario.
5. For headnodes, check disk usage `sudo du -ah --max-depth=1  / | sort -hr` for any high disk usage folders.
