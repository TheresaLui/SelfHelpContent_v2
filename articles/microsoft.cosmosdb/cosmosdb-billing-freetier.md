<properties
    pageTitle="Free Tier in Azure Cosmos DB"
    description="Free Tier in Azure Cosmos DB"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="jimsch"
    ms.author="jimsch"
    selfHelpType="generic"
    supportTopicIds="32738666"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    articleId="cosmosdb-billing-freetier"
    displayOrder="102"
    category="Security"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Free Tier in Azure Cosmos DB

Most users are able to resolve their Cosmos DB related Free Tier questions or issue using the steps below.


## **Recommended Steps**  

### **Free tier account limits**
- Number of free tier accounts per Azure subscription: *1*
- Duration of free-tier discount: *Lifetime of the account. Must opt-in during account creation.*
- Maximum RUs for free: *400 RUs*
- Maximum storage for free: *5 GB*
- Maximum number of shared throughput databases: *5*
- Maximum number of containers in a shared throughput database: *25 In free tier accounts, the minimum RUs for a shared throughput database with up to 25 containers is 400 RUs*


### **How does the Free Tier discount show up on my bill?**
In Free Tier accounts, you will get the first 400 RUs and 5 GB of storage in your account for free. Any RUs and storage beyond 400 RUs and 5 GB will be billed at the regular pricing rates per the pricing page. On the bill, you will not see a charge or line item for the free 400 RUs and 5 GB, only the RUs and storage beyond what is covered by free tier.  

### **Does Free Tier apply to all the Azure Cosmos DB APIs?**
Yes, Free Tier works for all Azure Cosmos DB APIs including Core (SQL), API for MongoDB, Cassandra, and Gremlin.   

### **Can I apply the Free Tier discount to autoscale databases and containers?**
**Answer:** Yes. With autoscale, you are billed for the highest RUs the database or container scales to in the hour. When the free tier discount is applied, 400 RUs will be subtracted from that value. See our documentation for examples and details.  

### **How does Free Tier discount work if I have an account with multiple regions?**
In multi-region accounts, the RUs of the database or container are replicated in all regions. For example, if you have a container with 400 RUs and the account is in 3 regions, the total RUs of the account is 1200 RUs. When the discount is applied, you will be billed for 1200 RUs ??? 400 RUs = 800 RUs per hour.  

### **Enable Free Tier when creating a new account in the Azure Portal is not appearing. Where is the option?**
**Solution: ** You can have up to one Free Tier account in an Azure subscription. If the option does not appear, this means another account in the subscription is already enabled with Free Tier.  



## **Recommended Documents**
[Build apps for free with Azure Cosmos DB Free Tier](https://devblogs.microsoft.com/cosmosdb/build-apps-for-free-with-azure-cosmos-db-free-tier/)
<br>Introducing Azure Cosmos DB Free Tier.  

[Free tier account limits](https://docs.microsoft.com/azure/cosmos-db/concepts-limits#free-tier-account-limits)
<br>Limits for Azure Cosmos DB free tier accounts.  




