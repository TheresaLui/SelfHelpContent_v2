<properties
    pageTitle="I'm having an issues with my YARN application"
    description="I'm having an issues with my YARN application"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
	ms.author="v-anukar"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32628998"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="MoonCake, Fairfax"
	articleId="6a063684-0c14-40eb-9be3-e0720ba788f6"
	ownershipId="AzureData_HDInsight"
/>

# I'm having issues with my YARN application

## **Recommended Steps**

To solve issues with YARN applications, the following articles might be helpful:

* **YARN Timeline Server**: The YARN Timeline server provides generic information on completed applications and framework-specific application information
* **YARN Application logs**: The application logs can be useful in debugging issues, with aggregated logs being stored in the path `/app-logs/<user>/logs/<applicationId>`
* **YARN CLI tools**: After connecting to HDInsight cluster using SSH, the YARN logs can be collected using `yarn logs -applicationId <applicationId> -appOwner <user-who-started-the-application>`
* **YARN ResourceManager UI**: Add `/yarnui/hn/logs/` to the end of the cluster URL to view the YARN logs 

## **Recommended Documents**

* [Access YARN application logs on Linux-based HDInsight](https://docs.azure.cn/hdinsight/hdinsight-hadoop-access-yarn-app-logs-linux)<br>
* [How do I download Yarn logs from HDInsight cluster?](https://hdinsight.github.io/yarn/yarn-download-logs.html)<br>
