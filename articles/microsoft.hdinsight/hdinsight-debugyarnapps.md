<properties
    pageTitle="I'm having an issues with my YARN application"
    description="I'm having an issues with my YARN application"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds="32511173"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="0b0579e2-2fdc-4472-818a-999cbd44f0ea"
	ownershipId="AzureData_HDInsight"
/>

# I'm having an issues with my YARN application

## **Recommended steps**
 In order to debug issues with YARN applications, the following aspects might be helpful.
 
 1. **YARN Timeline Server**: The YARN Timeline server provides generic information on completed applications and framework-specific application information..
 2. **YARN Application logs**: The application logs can be useful in debugging issues. The aggregated logs are stored in the path `/app-logs/<user>/logs/<applicationId>`
 3. **YARN CLI tools**: After connecting to HDInsight cluster using SSH, the YARN logs can be collected using: `yarn logs -applicationId <applicationId> -appOwner <user-who-started-the-application>`
 4. **YARN ResourceManager UI**: Add /yarnui/hn/logs/ to the end of the cluster URL to view the YARN logs 
 
## **Recommended documents**
[Access YARN application logs on Linux-based HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-access-yarn-app-logs-linux)<br>
[How do I download Yarn logs from HDInsight cluster?](https://hdinsight.github.io/yarn/yarn-download-logs.html)<br>
