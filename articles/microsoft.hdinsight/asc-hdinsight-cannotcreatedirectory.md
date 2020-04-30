<properties
    pageTitle="Cluster Error due to Ambari Agent cannot create a directory"
    description="Cluster Error due to Ambari Agent cannot create a directory"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="25"
    articleId="Hdi_CannotCreateDirectory"
    diagnosticScenario="HDInsightCannotCreateDirectoryInsight"
    selfHelpType="rca"
    supportTopicIds="32636418"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue

## Problem
<!--issueDescription-->
The following error <!--$Text-->[Text]<!--/$Text--> occurs when the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->'s Ambari cannot create a directory on the cluster. 
<!--/issueDescription-->

## **Recommended Steps**

In order to mitigate the issue please do the following:

* Ssh to affected node <!--$AlertHost-->[AlertHost]<!--/$AlertHost-->
* Get root user i.e. sudo su
* Recursively create needed directories
* Change owner and group for these folders:

```
$ chown -R yarn /mnt/resource/hadoop/yarn/local
$ chgrp -R hadoop /mnt/resource/hadoop/yarn/local
$ chown -R yarn /mnt/resource/hadoop/yarn/log
$ chgrp -R hadoop /mnt/resource/hadoop/yarn/log
```

* Go back to ambari portal. Click on this alert. Disable and enable the alert. This resets the alert status, which usually takes around 5 minutes.

## **Recommended Documents** 

* [Cannot create directory alert](https://hdinsight.github.io/ambari/Cannot-create-directory-alert.html)
