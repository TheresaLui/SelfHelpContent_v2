<properties
          pageTitle="Azure Storage Explorer"
          description="Azure Storage Explorer"
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
          articleId="8b5e2c87-e0c1-402e-944c-7a2cc1fd3533"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Azure Storage Explorer

**Move data with Storage Explorer**


1. **Download and Install** [Azure Storage Explorer](https://azure.microsoft.com/features/storage-explorer/) 
2. **Connect your account**
    1. In Storage Explorer, select View Account Management or select the Manage Accounts button. ACCOUNT MANAGEMENT now displays all the Azure accounts you've signed in to. 
    2. To connect to another account, select Add an account. 
    3. In Connect to Azure Storage, select an Azure cloud from Azure environment to sign in to a national cloud or an Azure Stack. 
    4. After you choose your environment, select Next.

3. **Copy data**
    1. In the left pane, expand the storage account containing the blob/file container you wish to manage. 
    2. Select the storage account and display the blob containers, file shares, tables or queues. 
    3. There is no way to copy/paste a storage account with all it's contents from one SA to another. 
    4. You will have to select the blob container, or file share and copy paste each one from source to destiny storage account.
    5. Storage explroer will use azcopy in the backend to perform those copy operations.

4. **Azure Storage Explorer troubleshooting guide**

    [This guide summarizes solutions for issues that are commonly seen in Storage Explorer](https://docs.microsoft.com/azure/storage/common/storage-explorer-troubleshooting)

<!---

questionAnswer
--

Question: 


**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1: Yes

2: No

-->


