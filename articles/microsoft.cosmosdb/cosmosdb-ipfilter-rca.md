<properties
    pageTitle="IP filter RCA"
    description="RCA - IP blocked by firewall"
    infoBubbleText="The IP address is not whitelisted for sending requests to the account. See the details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="rnagpal"
    ms.author="rnagpal"
    articleId="cosmosdb-ipfilter-rca"
    diagnosticScenario="CosmosDBIPFilterInsight"
    selfHelpType="rca"
    supportTopicIds="32636792"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# IP Blocked by Firewall

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The following IP addresses: **<!--$IPAddresses-->[IPAddresses]<!--/$IPAddresses-->** are not whitelisted for sending requests to the account: **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->**.
<!--/issueDescription-->

## **Recommended Steps**

It appears that your account has an IP access control policy which is restricting access to an IP range.

To configure IP policy-based access control, you must provide the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account. Once this configuration is applied, all requests originating from machines outside this allowed list are blocked by the server.

## **Recommended Documents**

* [Update the IP Access Control Policy](https://docs.microsoft.com/azure/cosmos-db/firewall-support)
