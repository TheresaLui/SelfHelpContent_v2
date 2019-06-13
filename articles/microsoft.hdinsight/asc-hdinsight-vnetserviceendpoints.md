<properties
    pageTitle="HDInsight VNet Service Endpoints"
    description="HDInsightVNetServiceEndpoints"
    infoBubbleText="Found recent VNet Service Endpoints error. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_Crud_MisconfiguredVnetServiceEndpoints"
    diagnosticScenario="HDInsightVNetServiceEndpointsInsight"
    selfHelpType="rca"
    supportTopicIds="32629129, 32636507"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

There is a problem with the virtual network service endpoints configured for your HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->. <br>
The client is trying to connect from IP address <!--$MissingIp-->[MissingIp]<!--/$MissingIp-->, which is not authorized to connect to the Azure SQL Database server. The server firewall has no IP address rule that allows a client to communicate from the given IP address to the SQL Database.

## **Recommended Steps**

1. Go to the SQL server’s “Firewalls and virtual networks” setting, turn on “Allow access to Azure services” or whitelist your virtual network which you used to deploy the HDI cluster. Pleaser refer to [Azure Portal Steps](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview#azure-portal-steps) for details.
2. On the Virtual Network side, [enable the SQL service endpoints](https://azure.microsoft.com/blog/vnet-service-endpoints-for-azure-sql-database-now-generally-available)
