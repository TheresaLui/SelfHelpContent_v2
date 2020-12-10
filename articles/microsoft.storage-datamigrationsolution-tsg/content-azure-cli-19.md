<properties
          pageTitle="Azure CLI"
          description="Azure CLI"
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
          articleId="2c5f6f8b-dbb2-477b-9857-9027301dc412"
           ownershipId="Centennial_CloudNet_LoadBalancer"
    />

# Azure CLI

**Move data with Azure CLI**


Azure CLI is an open source, cross platform set of tools for different azure services. 

<!---
Azure CLI, is a open source command-line tool providing a great experience for managing most of the Azure resources and not only Azure Storage. You can install it almost everywhere and, if you spend some time reading the command reference documentation, you can achieve almost anything you want.

-->

With regard to Azure Storage account management, all you need is **az storage** and the hundreds of options it provides, before uploading files or directories of files, it's important to have the Storage account name and the storage account key or the Storage Account's connection string. Let's see now some command lines to help you upload single files, multiple files or directories to an Azure Storage account blob container.

1. [Install Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest)

2. Upload Data

    **Upload single file with az storage blob upload**

      ```cli
      az storage blob upload -c <container_name> -f <path_to_your_file> -n <if_you_want_different_name> --account-name <storage_account_name> --account-key <storage_account_key>
      ```
    **Upload container with az storage blob upload**

      ```cli
      az storage blob upload -c <container_name> -f <path_to_your_file> -n <if_you_want_different_name> --account-name <storage_account_name> --account-key <storage_account_key>
      ```
    **Upload multiple files or directories with az storage blob upload-batch**

      ```cli
      az storage blob upload-batch -d <container_name> -s <directory_path> --pattern *.js --if-unmodified-since 2018-08-27T12:00Z --account-name <account_name> --account-key <account_key>
      ```


If you want to try your commands without actually uploading your files, you can add the `--dry-run` option at the end of your command.

<!---

questionAnswer
--

Question: 


**This is the end of the work flow. Did this TSG resolve your issue?**

Answers:

1: Yes

2: No

-->