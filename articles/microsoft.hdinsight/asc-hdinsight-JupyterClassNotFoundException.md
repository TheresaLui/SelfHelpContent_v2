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
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

There is a problem in copying of the storage jars to HTTPFS classpath is failing

## **Recommended Steps**

1. SSH to headnode0 in the cluster and run these scripts/Run this using script action

cp /usr/hdp/current/hadoop-client/hadoop-azure-2*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/hadoop-client/azure-data-lake-store-sdk-*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/hadoop-client/hadoop-azure-datalake-*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/lib/hdinsight-datalake/adls2-oauth2-token-provider-*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/hadoop-client/lib/jetty-util-*.hwx.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/spark2-client/jars/guice*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/spark2-client/jars/aopalliance-repackaged-2*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/spark2-client/jars/javax.inject-2*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/
cp /usr/hdp/current/hadoop-mapreduce-client/wildfly-openssl-*.jar /usr/hdp/current/hadoop-httpfs/webapps/webhdfs/WEB-INF/lib/

2. Restart Jupyter

## **Recommended Documents**

* [HDInsight Jupyter ClassNotFoundException](https://msdata.visualstudio.com/HDInsight/_wiki/wikis/HDInsight.wiki?pagePath=%2FWIKI%2FTSGs%2FSpark%2FNotebooks%2FJupyter%2FJupyter%20500%20ClassNotFoundException&pageId=2265&wikiVersion=GBwikiMaster)
