<properties
    pageTitle="Issues with Linux Custom Script extension"
    description="Issues with Linux Custom Script extension"
    service="microsoft.aksengine"
    resource="aksengine"
    authors="justinha"
    ms.author="justinha"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32689847"
    resourceTags=""
    productPesIds="16963"
    cloudEnvironments="public"
    articleId="aks-install-withlinuxcustomscriptextension"
/>

# Issues with Linux Custom Script extension

## **Recommended Steps**

1. Ensure your Cloud Operator has a supported AKS Engine version available in your Marketplace. For more information review the [Prerequisites for the AKS Engine](https://docs.microsoft.com/azure-stack/user/azure-stack-kubernetes-aks-engine-set-up#prerequisites-for-the-aks-engine)

2. If your installation method is failing, try the the [steps for a disconnected environment](https://docs.microsoft.com/azure-stack/user/azure-stack-kubernetes-aks-engine-deploy-linux#install-in-a-disconnected-environment)


### **Known Issues**

You must specify a supported Kubernetes version with the --version parameter when running the get-akse command. Link to the [supported versions](https://github.com/Azure/aks-engine/blob/master/docs/topics/azure-stack.md#supported-kubernetes-versions)


## **Recommended Documents**

* [Troubleshoot the AKS Engine on Azure Stack](https://docs.microsoft.com/azure-stack/user/azure-stack-kubernetes-aks-engine-troubleshoot)
* [AKS troubleshooting](https://docs.microsoft.com/azure/aks/troubleshooting)

