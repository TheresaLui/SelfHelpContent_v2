<properties
    pageTitle="Azure Virtual Network - Cannot delete VNet because of error message mentions ipconfigprofile"
    description="Azure Virtual Network - Cannot delete VNet because of error message mentions ipconfigprofile"
    service="microsoft.network"
    resource="virtualnetwork"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="generic"
    supportTopicIds="32781379"
    resourceTags=""
    productPesIds="15526"
    ownershipId="CloudNet_VirtualNetwork"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a776c3a8-b8bd-4c0f-9afa-8a2966f8951f"
/>

# Azure Virtual Network - Cannot delete VNet because of error message mentions ipconfigprofile

If you deployed Azure container instances, and have not cleaned up those resources, then delete the container instances before deleting the virtual network (VNet). If that does not help, follow these additional steps:

## **Recommended Steps**

1. In the Azure portal, go to the resource group's **Overview** page

2. In the header for the list of the resource group's resources, select **Show hidden types**. The network profile type is hidden in the Azure portal by default

3. Select the network profile related to the container groups

4. Select **Delete**

![Delete network profile](https://docs.microsoft.com/azure/virtual-network/media/virtual-network-troubleshoot-cannot-delete-vnet/container-instances.png)

Delete the subnet or virtual network again.

If these steps don't resolve the issue, use these Azure CLI commands to clean up resources:

1. Replace `{my-resource-group}`, `{my-vnet-name}`, and `{my-subnet-name}` with the name of your resource group, VNet, and subnet:

   `RES_GROUP={my-resource-group}`<br>
   `VNET_NAME={my-vnet-name}`<br>
   `SUBNET_NAME={my-subnet-name}`

2. Get the network profile ID:

   NetworkProfile=az network vnet subnet show -g $RES_GROUP --vnet-name $VNET_NAME --name $SUBNET_NAME -o tsv --query ipConfigurationProfiles[].id

3. Delete the network profile:

   `az network profile delete --ids $NetworkProfile --yes`

4. Delete the subnet:

   `az network vnet subnet delete --resource-group $RES_GROUP --vnet-name $ VNET_NAME --name $SUBNET_NAME`

5. Delete virtual network:

   `az network vnet delete --resource-group $RES_GROUP --name $SUBNET_NAME`

## **Recommended Documents**

- [Clean up resources](https://docs.microsoft.com/azure/container-instances/container-instances-vnet#clean-up-resources)
