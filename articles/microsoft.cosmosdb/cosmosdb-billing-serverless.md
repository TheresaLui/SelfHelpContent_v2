<properties
    pageTitle="Serverless"
    description="Troubleshoot Azure Cosmos DB Serverless issues"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32746033,32746032"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-billing-serverless"
    displayOrder="105"
    category="Billing and Pricing"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Serverless  
Most users are able to resolve their Cosmos DB related serverless questions or issues using the steps below.   

## **Recommended Steps**  


### **FAQ**

**I cannot create a serverless account with free tier**  
Cosmos DBs free tier can only be applied to provisioned capacity, not serverless accounts.   


**How can I update the throughput on my serverless container/collection/table/graph?**  
You do not have to provision any throughput in a serverless account as you only get billed for the Request Units consumed by your database operations.   


**How can I create a shared-throughput database in a serverless account?**  
You do not have to provision any throughput in a serverless account, so shared-throughput databases are not available.   


**My requests are getting throttled or are returning with a status code of 429**  
Serverless containers can currently deliver a maximum throughput of 5k RU/s.    


**I am getting the following error when trying to add data in my container: *Reached the maximum storage limit for the serverless container*.**    
During preview, a serverless container has a maximum storage size of 50 GB. This error indicates that you have hit the maximum storage limit for your container.   


**How can I add more Azure regions to my serverless account?**  
During public preview, it is not possible to add Azure regions to a serverless account.   


**How can I enable the Synapse Link preview on my serverless account?**  
During public preview, it is not possible to enable the Synapse Link preview on a serverless account.  


**I can not find the *Throughput*, *Availability*, *Latency* or *Consistency* tabs in the metrics shown in the portal**  
- There is no *Throughput* tab because serverless resources do not require any throughput management. 
- The *Availability*, *Latency* and *Consistency* tabs are not shown because there is no SLA guarantee for preview features.




## **Recommended Documents**  

[Build apps of any size or scale with Azure Cosmos DB](https://azure.microsoft.com/blog/build-apps-of-any-size-or-scale-with-azure-cosmos-db/)
<br>Announcement Blog.  

