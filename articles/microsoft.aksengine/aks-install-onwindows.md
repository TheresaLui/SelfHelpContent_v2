<properties
    pageTitle="Issues installing AKS Engine on Linux"
    description="Issues installing AKS Engine on Linux"
    service="microsoft.aksengine"
    resource="aksengine"
    authors="justinha"
    ms.author="justinha"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32689845"
    resourceTags=""
    productPesIds="16963"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="aks-install-onwindows"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Issues installing AKS Engine on Linux

## **Recommended Steps**

1. Ensure your Cloud Operator has a supported AKS Engine version available in your Marketplace. For more information review the [Prerequisites for the AKS Engine](https://docs.microsoft.com/azure-stack/user/azure-stack-kubernetes-aks-engine-set-up#prerequisites-for-the-aks-engine).

2. If your installation method is failing, try the the [steps for a disconnected environment](https://docs.microsoft.com/azure-stack/user/azure-stack-kubernetes-aks-engine-deploy-linux#install-in-a-disconnected-environment)

### **Known Issues**

You must specify a [supported Kubernetes version](https://github.com/Azure/aks-engine/blob/master/docs/topics/azure-stack.md#supported-kubernetes-versions) with the `--version` parameter when running the `get-akse` command.


## **Recommended Documents**

* [Troubleshoot the AKS Engine on Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-kubernetes-aks-engine-troubleshoot)
* [AKS troubleshooting](https://docs.microsoft.com/azure/aks/troubleshooting)

