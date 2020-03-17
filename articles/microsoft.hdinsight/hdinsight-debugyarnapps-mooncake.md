<properties
    pageTitle="I'm having an issues with my YARN application"
    description="I'm having an issues with my YARN application"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    ms.author="bharathb"
    displayOrder="9"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="hdinsight-debugyarnapps-mooncake"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# I'm having an issues with my YARN application

## **Recommended Steps**
 In order to debug issues with YARN applications, the following aspects might be helpful.
 
 1. **YARN Timeline Server**: The YARN Timeline server provides generic information on completed applications and framework-specific application information
 2. **YARN Application logs**: The application logs can be useful in debugging issues. The aggregated logs are stored in the path `/app-logs/<user>/logs/<applicationId>`.
 3. **YARN CLI tools**: After connecting to HDInsight cluster using SSH, the YARN logs can be collected using: `yarn logs -applicationId <applicationId> -appOwner <user-who-started-the-application>`
 4. **YARN ResourceManager UI**: Add /yarnui/hn/logs/ to the end of the cluster URL to view the YARN logs 
 
## **Recommended Documents**

* [Access YARN application logs on Linux-based HDInsight](https://docs.azure.cn/hdinsight/hdinsight-hadoop-access-yarn-app-logs-linux)
* [How do I download Yarn logs from HDInsight cluster?](https://hdinsight.github.io/yarn/yarn-download-logs.html)
