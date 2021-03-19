<properties
    pageTitle="Azure Virtual Network - Utilize Service Tags in NSG rules"
    description="Azure Virtual Network - Utilize Service Tags in NSG rules"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781397"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="587918ba-99a8-41bb-97ed-99f7fc62dfab"
/>

# Azure Virtual Network - Utilize Service Tags in NSG rules

## **Recommended Steps**

1. To understand which internet protocals (IPs) belong to Microsoft services, see the mapping of IP ranges to Service Tags in the [weekly JSON download]( https://docs.microsoft.com/azure/virtual-network/service-tags-overview#discover-service-tags-by-using-downloadable-json-files). This file is updated every Monday. All IPs in the Azure cloud address space can be found under the AzureCloud tag.
2. The Discovery API (Get-AzNetworkServiceTags and az network list-service-tags) commands are currently in Public Preview. The API may return incorrect and/or incomplete results until it is released for general audiences
3. To restrict traffic to and from specific Microsoft services, see the [Service Tag documentation](https://docs.microsoft.com/azure/virtual-network/service-tags-overview) for a list of Service Tags and how they are used in network security group (NSG) rules
4. You can't currently create User Defined Routes with Service Tags as the IP Prefix field. See [Virtual network service tags](https://docs.microsoft.com/azure/virtual-network/service-tags-overview) for the status on this feature ask.
5. If a Service Tag is missing from the Portal selection blade for Network Security Group rule creation, check whether the tag is listed in our public document. Only Service Tags present in this table can be found in the Portal (except where noted).

## **Recommended Documents**

- [Service Tag overview](https://docs.microsoft.com/azure/virtual-network/service-tags-overview)
- [Service Tag example with Storage tag](https://docs.microsoft.com/azure/virtual-network/tutorial-restrict-network-access-to-resources)
- [Get-AzNetworkServiceTags](https://docs.microsoft.com/powershell/module/az.network/get-aznetworkservicetag?view=azps-5.0.0)
- [az network list-service-tags](https://docs.microsoft.com/cli/azure/network?view=azure-cli-latest#az_network_list_service_tags)
