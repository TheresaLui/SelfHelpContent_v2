<properties 
    pageTitle="Kernel Disconnect Error in Integrated Notebooks"
    description="Kernel Disconnect Error in Integrated Notebooks"
    service="microsoft.machinelearning"
    resource="computeinstance"
    authors="hustcrystal"
    ms.author="chrjia, femi.olukoya"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32690895"
    resourceTags="notebook,computeinstance"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    articleId="microsoft.machinelearning.computeinstance.kerneldisconnect"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Kernel Disconnect Error in Integrated Notebooks

- Integrated notebooks aren't working in workspace 2.0 (but they work from the vm/ci itself in Jupyter)
- This affects primarily the UI and Notebooks
- How to mitigate this problem and the eventual resolution

## **Recommended Steps**

- Workaround 1: Use Jupyter from the Compute Instance/Notebook VM instead
- Workaround 2: Try restarting the Compute Instance/Notebook VM and then rerunning the notebook
