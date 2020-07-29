<properties
    pageTitle="Azure HPC Cache Installation and Setup Issues"
    description="Resolve installation and setup issues with the Azure HPC Cache."
    infoBubbleText="Azure HPC Cache Installation and Setup Issues"
    authors="cfriedel"
    ms.author="clfriede"
    displayOrder="1"
    articleId="storagecache-installationandsetup"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32674485"
    resourceTags=""
    productPesIds="16790"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="StorageMediaEdge_HPCCache"
/>

# Azure HPC Cache Installation and Setup Issues

Most customers can resolve installation and setup issues by following the [Azure HPC Cache Documentation](https://docs.microsoft.com/azure/hpc-cache/). You will need to complete the following steps to install the Azure HPC Cache: Configuring Prerequisites, Create the Cache, Add Storage, and Mount Clients.

## **Recommended Steps**

1. A large part of installing the HPC Azure Cache involves planning and preparing your environment for the installation of the Azure HPC Cache. Reviewing the [prerequisites](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-prereqs) and [planning the namespace](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-namespace) will help make the installation of the HPC cache easier.  

2. Once you have completed the prerequisite tasks and have planned your namespace, you should then move on to [creating the cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-create). If you have completed the creation of the cache successfully, you should now have an Azure HPC Cache resource that should be in a healthy state.

3. Once you have finished creating an Azure HPC Cache resource, the next step is to [add storage targets](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-add-storage). Adding storage targets to the Azure HPC Cache allows you to create the namespace that you have planned previously.

4. Once you have created your storage targets and namespace, you can then have clients [connect to the cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-mount)

5.  Once you have completed the steps above, you should then be able to [monitor the Azure HPC Cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-manage) using the Azure Portal

## **Recommended Documents**

* [Azure HPC Cache Documentation](https://docs.microsoft.com/azure/hpc-cache/)
* [Azure HPC Cache Prerequisites](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-prereqs)
* [Planning the Namespace](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-namespace)
* [Creating an Azure HPC Cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-create)
* [Adding Storage Targets](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-add-storage)
* [Connecting clients to the Azure HPC Cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-mount)
* [Monitoring the Azure HPC Cache](https://docs.microsoft.com/azure/hpc-cache/hpc-cache-manage)
