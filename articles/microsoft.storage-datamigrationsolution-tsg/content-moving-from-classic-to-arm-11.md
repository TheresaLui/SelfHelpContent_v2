<properties
          pageTitle="Moving from Classic to ARM"
          description="Moving from Classic to ARM"
          service="Microsoft.Storage"
          resource="Microsoft.Storage/storageAccounts"
          authors="akshaymatmicrosoft"
          ms.author="akshaym"
          displayOrder=""
          selfHelpType="TSG_Content"
          supportTopicIds=""
          resourceTags=""
          productPesIds=""
          cloudEnvironments="public, fairfax, usnat, ussec"
          articleId="7d4e9b17-f399-4c9b-8a54-a64a2f3eb3e0"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Moving from Classic to ARM

**Data migration from Moving from Classic to ARM**

The best and fastest solution is to migrate the storage account and not the content within the storage account if possible. 

1. Data migration from Classic Storage Account to ARM Storage Account

2. Customer wants to migrate data from classic storage account to an ARM Storage Account

3. The below articles provide information on moving from a Classic Storage Account to Azure Resource Manager Storage Account using:


    **PowerShell**: 
    [Migrate a storage account](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-ps#step-52-migrate-a-storage-account)

    **Azure CLI**: [Migrate a storage account](https://docs.microsoft.com/azure/virtual-machines/linux/migration-classic-resource-manager-cli#step-5-migrate-a-storage-account)

    *Note: There are additional steps to move a Virtual Machine, which is out of the scope of this document*

<!---

There are many different tools and commands that you can use to move data to, from, and within Azure Storage.

This article is intended to document these options, and provide links to helpful articles which explain how to choose an ideal Data Migration Solution.

Use this TSG for a request to migrate the storage accounts from classic to arm

As you follow through the steps in this TSG, maintain notes of each command run and output generated. 

Should you run into any difficulties, this information will be critical to determine next steps.


questionAnswer
--

Question: 


**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1: Yes
2: No

-->



