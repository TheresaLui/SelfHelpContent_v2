<properties
    pageTitle="Private IP filter RCA"
    description="RCA - Private IP blocked by firewall"
    infoBubbleText="The virtual network or private endpoint is not whitelisted for sending requests to the account."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-privateipfilter-rca"
    diagnosticScenario="CosmosDBPrivateIPFilterInsight"
    selfHelpType="rca"
    supportTopicIds="32636765, 32636824, 32675641, 32636792, 32738664, 32636750, 32636769, 32636776, 32636770, 32681470, 32636777, 32681008, 32636771, 32636778, 32636778, 32738665"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# <!--$ReasonBlocked-->[ReasonBlocked]<!--/$ReasonBlocked--> Blocked by Firewall

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
Some **<!--$ReasonBlocked-->[ReasonBlocked]<!--/$ReasonBlocked-->** that are not whitelisted for sending requests to the account: **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->** have been blocked.
<!--/issueDescription-->

## **Recommended Steps**

It appears that your account has an IP access control policy that is restricting access to <!--$ReasonBlocked-->[ReasonBlocked]<!--/$ReasonBlocked-->. Please ensure you are accessing the account from whitelisted <!--$ReasonBlocked-->[ReasonBlocked]<!--/$ReasonBlocked-->.

## **Recommended Documents**

* [Configure virtual network access](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-vnet-service-endpoint)
* [Configure private endpoint access](https://docs.microsoft.com/azure/cosmos-db/how-to-configure-private-endpoints)
