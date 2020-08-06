<properties
    pageTitle="I am unable to delete a Cluster or Resource Group"
    description="I am unable to delete a Cluster or Resource Group"
    service="microsoft.aksengine"
    authors="v-miegge"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32689833"
    resourceTags=""
    productPesIds="16963"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="e284c87e-b625-4201-89be-eaa6ff7b22a2"
	ownershipId="Compute_AzureKubernetesService"
/>

# I am unable to delete a Cluster or Resource Group

## **Recommended Steps**

To delete the cluster itself, use the **az group** delete command to delete the AKS resource group:

```
az group delete --name myResourceGroup --yes --no-wait
```

## **Recommended Documents**

* [Cleanup resources](https://docs.microsoft.com/azure/aks/use-multiple-node-pools#clean-up-resources)
