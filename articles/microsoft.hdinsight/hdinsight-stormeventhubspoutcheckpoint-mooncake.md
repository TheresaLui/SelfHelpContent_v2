<properties
    pageTitle="Transfer Storm eventhub spout checkpoint info"
    description="Transfer Storm eventhub spout checkpoint info"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    ms.author="bharathb"
    displayOrder="36"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="hdinsight-stormeventhubspoutcheckpoint-mooncake"
/>

# Transfer Storm eventhub spout checkpoint information from one topology to another

When developing topologies that read from eventhubs using HDInsight’s Storm eventhub spout jar, one can deploy a topology with the same name on a new cluster, but retain the checkpoint data committed to zookeeper in the old cluster. 

## **Recommended documents**

[Transfer Storm eventhub spout checkpoint info](https://hdinsight.github.io/storm/import-export-eventhub-spout-checkpoint-data.html)
