<properties
    pageTitle="Integrated Service Environment - Network Health"
    description="Integrated Service Environment - Network Health"
    service="microsoft.ise"
    resource=""
    authors="v-miegge"
    ms.author="kawilson"
    selfHelpType="generic"
    supportTopicIds="32780464"
    resourceTags=""
    productPesIds="17030"
    ownershipId="Compute_LogicApps"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="3bd0bc8a-9842-490f-ba56-b9af0f066188"
/>

# Integrated Service Environment - Network Health

Managing your integration service environment (ISE) network health in Azure Logic Apps

If you use ExpressRoute, which provides a private connection to Microsoft cloud services that's facilitated by the connectivity provider, you must create a route table that has the following route and link that table to each subnet that's used by your ISE:

Name: < route-name ><BR>
Address prefix: 0.0.0.0/0<BR>
Next hop: Internet<BR>

## **Recommended Documents**

- [What network ports are used by your ISE](https://docs.microsoft.com/azure/logic-apps/connect-virtual-network-vnet-isolated-environment#network-ports-used-by-your-ise)
- [Set up ISE Endpoint access](https://docs.microsoft.com/azure/logic-apps/connect-virtual-network-vnet-isolated-environment-overview#endpoint-access)
- [Setting up name resolution for resources in Azure virtual networks](https://docs.microsoft.com/azure/virtual-network/virtual-networks-name-resolution-for-vms-and-role-instances)
