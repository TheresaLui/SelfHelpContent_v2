<properties
    pageTitle="Integrated Service Environment - Network Health"
    description="Integrated Service Environment - Network Health"
    service="microsoft.logicapps"
    resource="logicapps"
    authors="v-miegge"
    ms.author="kawilson"
    selfHelpType="generic"
    supportTopicIds="32742533"
    resourceTags=""
    productPesIds="15791"
    ownershipId="Compute_LogicApps"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="db7a05ef-1dee-4a89-931e-c9c83f3b84eb"
/>

# Integrated Service Environment - Network Health

Manage your integration service environment (ISE) network health in Azure Logic Apps.

ExpressRoute provides a private connection to Microsoft cloud services that's facilitated by the connectivity provider. If you use this, you must create a route table that has the following route, and link that table to each subnet used by your ISE.

Name: <route-name>
Address prefix: 0.0.0.0/0
Next hop: Internet

## **Recommended Documents**

- [Network ports used by your ISE](https://docs.microsoft.com/azure/logic-apps/connect-virtual-network-vnet-isolated-environment#network-ports-used-by-your-ise)
- [Set up ISE Endpoint access](https://docs.microsoft.com/azure/logic-apps/connect-virtual-network-vnet-isolated-environment-overview#endpoint-access)
- [Set up name resolution for resources in Azure virtual networks](https://docs.microsoft.com/azure/virtual-network/virtual-networks-name-resolution-for-vms-and-role-instances)

