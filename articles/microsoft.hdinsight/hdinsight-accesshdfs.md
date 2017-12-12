<properties
    pageTitle="Access HDFS from the cluster"
    description="Access HDFS from the cluster"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathb"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
/>

# Access HDFS from the cluster

## **Recommended steps**
In order to access local HDFS instead of WASB or ADLS from inside the HDInsight cluster, use either of the two steps.

1. From Command line: Use the command - `hdfs dfs -D "fs.default.name=hdfs://mycluster/" <commandName>`
2. From Applications: Use the hdfs uri as "hdfs://mycluster/" while accessing the file system from the application
