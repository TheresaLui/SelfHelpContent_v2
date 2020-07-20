<properties
    pageTitle="HDInsight Jupyter service is down in headnode in ambari page"
    description="Jupyter service is down in headnode in ambari page is because the port is already in use"
    infoBubbleText="Found recent service is down in in ambari. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="Sainath"
    ms.author="v-samaly"
    displayOrder=""
    articleId="HDI_JupyterPortInUse"
    diagnosticScenario="HDInsightJupyterPortAlreadyInUseInsight"
    selfHelpType="rca"
    supportTopicIds="32636430"
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

* The default port for Jupyter notebook in HDI is 8001
* Directory `var/run/jupyter/` should exist in headnode0 (hn0), and should contain a file jupyter.pid which is created by OS to store the pid for jupyter. It gets deleted when process dies.

	* Check if `var/run/jupyter/` exists
	* If yes, delete the file jupyter.pid
	* If no, create this folder and run this command to change its ownership to root: `sudo chown /run/jupyter spark:root`
	* Kill the process listening on port 8001 using this command (assuming 18816 is the process taking port 8001): `sudo kill -9 18816`
	* To know the process taking port 8001, you can use `netstat -tlup | grep 8001`
	* Restart the jupyter
