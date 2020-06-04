<properties
    pageTitle="Access HDFS from the cluster"
    description="Access HDFS from the cluster"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathb"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636425"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
    articleId="bb094bd0-f9c8-49d7-86d3-8be6432d30c4"
	ownershipId="AzureData_HDInsight"
/>

# Access HDFS from the cluster

## **Recommended Steps**

In order to access local HDFS instead of WASB or ADLS from inside the HDInsight cluster, use either of these two steps:

1. From Command line: Use the command - `hdfs dfs -D "fs.default.name=hdfs://mycluster/" <commandName>`
2. From Applications: Use the hdfs uri as "hdfs://mycluster/" while accessing the file system from the application
