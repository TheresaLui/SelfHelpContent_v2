<properties
    pageTitle="Azure HDInsights: My hive queries are really slow"
    description="My hive queries are really slow"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    ms.author="bharathb, jaserano, deeptivu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636458"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public,MoonCake, Fairfax, usnat, ussec"
    articleId="913102d6-193a-48b4-b259-64fd4927379e"
	ownershipId="AzureData_HDInsight"
/>

# Hive Performance

## **Recommended Steps**

The following Hive performance optimization methods can be applied to your cluster:

 1. Scale out your worker nodes to leverage more mappers and reducers to be run in parallel
 2. Enable Tez as the execution engine instead of MapReduce
 3. Review your partitioning scheme to consider cases where there are too few or too many partitions. Choose the scheme such that the partitions are evenly sized.
 4. Use the ORCFile format which is optimized for faster access to data
 5. Enable vectorization to process multiple rows together
 
 To troubleshoot query or job performance:
 
* Follow the query execution through the role and application logs and also the query plan, check which part takes the longest and start analyzing from there. Hive provides an EXPLAIN command that shows the execution plan for a query: `EXPLAIN EXTENDED <query>`
* Look for <PerfLog> entries in the role logs (By default, role logs are located at `/var/log/hive/`). Example collection scripts:
    
    * tar cvfz /tmp/hs2_role_logs_`hostname -f`.tgz /var/log/hive/*HIVESERVER2*
    * tar cvfz /tmp/hms_role_logs_`hostname -f`.tgz /var/log/hive/*HIVEMETASTORE*
    
* If Hive is not responding, the established test of the conditions of "not responding" can be validated by:

    1. Connecting to HiveServer2 through Beeline
    2. Issue the command `>show databases`

    **Note**:  HiveServer2 is considered slow or unresponsive if the command takes more than 50 seconds to return.  If the command returns in less than 50 seconds, investigate the query that is reporting the problem.

## **Recommended Documents**

* [Optimize Apache Hive queries in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-optimize-hive-query)

### **Troubleshooting**

* [Why is my reducer extremely slow?](https://hdinsight.github.io/hive/hive-slow-reducer.html)
* [Why does Tez application hang?](https://hdinsight.github.io/hive/hive-tez-job-hang.html)
