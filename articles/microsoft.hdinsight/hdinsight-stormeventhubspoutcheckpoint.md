<properties
    pageTitle="Transfer Storm eventhub spout checkpoint info"
    description="Transfer Storm eventhub spout checkpoint info"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    displayOrder="15"
    selfHelpType="resource"
    supportTopicIds="32511223"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax"
	articleId="5df0937d-cc30-41f5-8354-bea63dde782e"
	ownershipId="AzureData_HDInsight"
/>

# Transfer Storm eventhub spout checkpoint information from one topology to another
When developing topologies that read from eventhubs using HDInsight’s Storm eventhub spout jar, one can deploy a topology with the same name on a new cluster, but retain the checkpoint data committed to zookeeeper in the old cluster. 


## **Recommended documents**
[Transfer Storm eventhub spout checkpoint info](https://hdinsight.github.io/storm/import-export-eventhub-spout-checkpoint-data.html)<br>
