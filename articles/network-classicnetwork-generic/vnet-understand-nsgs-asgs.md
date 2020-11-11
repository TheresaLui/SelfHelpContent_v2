<properties
    pageTitle="Azure Virtual Network - Understand NSGs and ASGs"
    description="Azure Virtual Network - Understand NSGs and ASGs"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781395"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="18aaa846-e694-4d3d-904f-19290e702c08"
/>

# Azure Virtual Network - Understand NSGs and ASGs

## **Recommended Steps**

1. Azure security groups can't be moved from one region to another. Use an Azure Resource Manager (ARM) template to export the existing configuration and security rules of a network security group (NSG). See [Move Azure network security group (NSG) to another region using the Azure portal]( https://docs.microsoft.com/azure/virtual-network/move-across-regions-nsg-portal) for detailed steps.

2. For issues deleting an NSG, make sure that that you have dissociated it from all subnets and network interfaces. See [Associate or dissociate a network security group]( https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface#associate-or-dissociate-a-network-security-group) for detailed steps.

3. See the [Azure subscription limits document](https://docs.microsoft.com/azure/azure-resource-manager/management/azure-subscription-service-limits#networking-limits) for detailed information on the number of NSGs and application security groups (ASGs) allowed per subscription and other related limits. Learn how to [check your current usage against these limits](https://docs.microsoft.com/azure/networking/check-usage-against-limits).

4. For help deploying NSGs and ASGs via Azure Resource Manager (ARM) templates, see our [Quickstart templates](https://azure.microsoft.com/resources/templates/?term=NSG) for common deployment scenarios

5. For issues and questions related to Terraform and NSGs, see the Terraform section of the [HashiCorp community portal](https://discuss.hashicorp.com/search?q=NSG%20category%3A27%20order%3Alatest)

6. Visit [What is an endpoint access control list?](https://docs.microsoft.com/previous-versions/azure/virtual-network/virtual-networks-acl) to understand the differences between Classic access control lists (ACLs) and ARM NSGs

7. Check the [status of common NSG and ASG feature asks](https://feedback.azure.com/forums/217313-networking?category_id=77468)

## **Recommended Documents**

- [Understanding NSGs](https://docs.microsoft.com/azure/virtual-network/network-security-groups-overview)
- [Understanding ASGs](https://docs.microsoft.com/azure/virtual-network/application-security-groups)
- [Managing NSGs](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group)
- [Migrating NSGs](https://docs.microsoft.com/azure/virtual-network/move-across-regions-nsg-portal)
- [Understanding subscription limits on ASGs and NSGs](https://docs.microsoft.com/azure/azure-resource-manager/management/azure-subscription-service-limits#networking-limits)
