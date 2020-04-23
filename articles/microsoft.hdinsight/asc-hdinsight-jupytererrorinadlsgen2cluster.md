<properties
    pageTitle="HDInsight Insight to determine if ADLSGen2 Cluster has Jupyter error because hadoop-httpfs failed to start"
    description="hadoop-httpfs failed to start in Jupyter notebook API for clusters with ADLSGen2 file storage"
    infoBubbleText="Found jupyter error in cluster. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="Sainath"
    ms.author="v-samaly"
    displayOrder=""
    articleId="HDI_JupyterSystemdErrorInHDI4.0ADLSGen2Cluster"
    diagnosticScenario="HDInsightJupyterErrorAsHadoopHTTPFSStartFailedInsight"
    selfHelpType="rca"
    supportTopicIds="32636498, 32636484"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Jupyter service for your HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is down. Jupyter depends on a systemd service called "hadoop-httpfs", which failed to start.
<!--/issueDescription-->

## **Recommended Steps**

* SSH to headnode0 in the cluster and run these scripts:

```
sudo sed -i "s/HttpFSContentsManager.root = 'HdiNotebooks'/#HttpFSContentsManager.root = 'HdiNotebooks'/" /var/lib/.jupyter/jupyter_notebook_config.py
sudo sed -i "s/c.NotebookApp.contents_manager_class = HttpFSContentsManager/#c.NotebookApp.contents_manager_class = HttpFSContentsManager/" /var/lib/.jupyter/jupyter_notebook_config.py
sudo sed -i "s/use_httpfs = not cluster_utilities.is_wasb_primary_fs()/use_httpfs = False/" /var/lib/ambari-server/resources/common-services/JUPYTER/1.0.0/package/scripts/jupyter.py
```

* Restart Jupyter from Ambari UI
