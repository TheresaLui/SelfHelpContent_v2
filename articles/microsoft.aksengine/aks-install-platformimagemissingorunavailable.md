<properties
    pageTitle="Platform Image is missing or unavailable"
    description="Platform Image is missing or unavailable"
    service="microsoft.aksengine"
    resource="aksengine"
    authors="justinha"
    ms.author="justinha"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32689855"
    resourceTags=""
    productPesIds="16963"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="aks-install-platformimagemissingorunavailable"
	ownershipId="Compute_AzureKubernetesService"
/>

# Platform Image is missing or unavailable

## **Recommended Steps**

1. To use the AKS Engine, the Azure Stack operator is responsible for downloading the required marketplace items and the creation of a service principal identity. For more information, see [prerequisites for the AKS engine](https://docs.microsoft.com/azure-stack/user/azure-stack-kubernetes-aks-engine-set-up#prerequisites-for-the-aks-engine).

2. The AKS Engine version depends on a specific image version that you can make available in your Azure Stack. To check the AKS Engine versions and corresponding Kubernetes version, see [Supported Kubernetes Versions](https://github.com/Azure/aks-engine/blob/master/docs/topics/azure-stack.md#supported-kubernetes-versions).


## **Recommended Documents**

* [Troubleshoot the AKS Engine on Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-kubernetes-aks-engine-troubleshoot)
* [AKS troubleshooting](https://docs.microsoft.com/azure/aks/troubleshooting)

