<properties
    pageTitle="Delete HDInsight Cluster"
    description="TSG / How-to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636445"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
    articleId="hdinsight-delete-cluster"
/>
# Common Solutions to HDInsight Delete Issues

When attempting to delete an HDInsight cluster, customers may encounter the following error:

*Conflict (HTTP Status Code: 409) error when attempting to delete a cluster immediately after creation of a cluster. If you encounter this error, please wait until the newly created cluster is in operational state before attempting to delete it.*

If you are unable to delete your cluster in **PowerShell**:

* Use the following command and ensure that you are using supported parameters.

    ```Remove-AzureRmHDInsightCluster -ClusterName CLUSTERNAME```

* When using the command, replace ```CLUSTERNAME``` with the name of your HDInsight cluster.

For more information on using these parameters, visit [Use-AzureRmHDInsightCluster](https://docs.microsoft.com/powershell/module/azurerm.hdinsight/use-azurermhdinsightcluster?view=azurermps-6.13.0).

Also, verify that you do not have any locks on your resource. For more information, visit [Lock resources to prevent unexpected changes](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#portal).

HDInsight cluster billing starts once a cluster is created and stops when the customer issues a delete request. Billing is pro-rated per minute, so you should always delete your cluster when it is no longer in use.

Customers may also receive the error: *Cannot delete cluster due to Cluster Name already in use*

This can occur if:

* The delete operation has not completed yet. <br>
  * Please allow time for the delete operation to complete.<br>
* The cluster name has been used by another customer.<br>
  * Always use unique cluster names.

If you are using custom scripts to delete cluster, please use [these templates](https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/hdinsight/hdinsight-hadoop-create-linux-clusters-arm-templates.md).

There is currently no way to start and stop an HDInsight cluster. Instead, you must create the cluster when required, and then delete the cluster when no longer needed.

## **Recommended Documents**

* [Delete an HDInsight cluster using your browser, PowerShell, or the Azure Classic CLI](https://docs.microsoft.com/azure/hdinsight/hdinsight-delete-cluster)
