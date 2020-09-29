<properties
    pageTitle="HDInsight Insight to determine if ADLS or wasbs based Cluster has Jupyter error because hadoop-httpfs failed to start"
    description="hadoop-httpfs failed to start in Jupyter notebook API for clusters with ADLS or wasbs file storage"
    infoBubbleText="Found jupyter error in cluster. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="Sainath"
    ms.author="v-samaly"
    displayOrder=""
    articleId="HDI_JupyterSystemdErrorInADLSOrWASBSCluster"
    diagnosticScenario="HDInsightJupyterErrorAsSystemdStartFailedInGen1ClusterInsight"
    selfHelpType="rca"
    supportTopicIds="32636498, 32636484"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue

<!--issueDescription-->
Jupyter service for your HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is down.
<!--/issueDescription-->

## **Recommended Steps**

Jupyter depends on a systemd service called "hadoop-httpfs", which failed to start.

SSH to headnode0 in the cluster and run these scripts:

```
sudo sed -i "s#^ExecStartPre=/bin/sh -c 'test -d \\\$HTTPFS_RUN || mkdir -p \\\$HTTPFS_RUN'#ExecStartPre=/bin/sh -c 'test -d \\\$HTTPFS_RUN || mkdir -p \\\$HTTPFS_RUN; chown httpfs \\\$HTTPFS_RUN; chgrp hadoop \\\$HTTPFS_RUN'\nPermissionsStartOnly=true#g" /usr/lib/systemd/system/hadoop-httpfs.service
```
