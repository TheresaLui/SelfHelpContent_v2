<properties
    pageTitle="HDInsight Jupyter ClassNotFoundException"
    description="Copying of the storage jars to HTTPFS classpath is failing and giving ClassNotFoundException"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="Ravi"
    ms.author="v-ravikc"
    displayOrder=""
    articleId="Hdi_JupyterClassNotFoundException"
    diagnosticScenario="HDInsightJupyterClassNotFoundExceptionInsight" 
    selfHelpType="rca"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue

<!--issueDescription-->
Copying of the storage jars to HTTPFS classpath is failing.
<!--/issueDescription-->

## **Recommended Steps**

1. SSH to headnode0 in the cluster and run these scripts using script action:

```
cp /usr/hdp/current/hadoop-client/hadoop-azure-2*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/hadoop-client/azure-data-lake-store-sdk-*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/hadoop-client/hadoop-azure-datalake-*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/lib/hdinsight-datalake/adls2-oauth2-token-provider-*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/hadoop-client/lib/jetty-util-*.hwx.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/spark2-client/jars/guice*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/spark2-client/jars/aopalliance-repackaged-2*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/spark2-client/jars/javax.inject-2*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/hadoop-mapreduce-client/wildfly-openssl-*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/

```

2. Restart Jupyter

