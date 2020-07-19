<properties
    pageTitle="I am unable to delete Cluster or Resource Group"
    description="I am unable to delete Cluster or Resource Group"
    service="microsoft.containerservices"
    resource="managedclusters"
    authors="v-miegge, ChiragPavecha"
    ms.author="chiragpa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32637191"
    resourceTags="linux"
    productPesIds="16450"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="06fdeb5e-84a4-482f-9eee-39eaa56bf617"
	ownershipId="Compute_AzureKubernetesService"
/>

# Kubernetes Service

## **Recommended Documents**

### Common causes for failed Cluster deletion<br>

* [Unable to delete as Public IP address is still in use](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address#view-change-settings-for-or-delete-a-public-ip-address)<br>
* [Azure Kubernetes Services stuck in Creating or Deleting State](https://docs.microsoft.com/azure/aks/troubleshooting#im-receiving-errors-when-trying-to-create-update-scale-delete-or-upgrade-cluster-that-operation-is-not-allowed-as-another-operation-is-in-progress)<br>
* ["AuthorizationFailed" error while trying to delete the AKS cluster](https://stackoverflow.com/questions/46921036/unable-to-delete-aks-cluster)<br>

### Walk-through article<br>

* [How to delete an AKS cluster](https://docs.microsoft.com/cli/azure/aks?view=azure-cli-latest#az-aks-delete)<br>

### AKS Support Policy<br>

* [Azure Kubernetes Service support policies](https://docs.microsoft.com/azure/aks/support-policies#azure-kubernetes-service-support-coverage)
