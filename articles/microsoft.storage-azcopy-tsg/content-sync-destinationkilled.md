<properties
	pageTitle="Sync DestinationKilled"
	description="Sync DestinationKilled"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8025eb88-7887-4197-8a66-600dadda2ec3"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Sync DestinationKilled

1. Customer is attempting to utilize the AzCopy Sync cmdlet to synchronize a large number of files between a storage account located in North Europe with an account located in UAE. You'll notice the scanning of files may halt, or gets interrupted with an error stating "DestionationlKilled". The scan may still progress but not complete. 
2. Caused by performance constraints in the environment 
3. There are five possible solutions:
   1. Add memory to the machine where he's running it. (Easy if its an on-prem VM, harder if its a physical machine) 
   2.  Get a big Azure VM and use that. One with lots of RAM. 
   3. Break the work up. E.g. if the source container contains, say, 20 subfolders, do the subfolders one at a time. 
   4. Use copy instead of sync. I see that the customer is using the default sync settings. (I.e. no extra parameters). So, to reduce memory usage they can use "azcopy copy" with this added to the command line: -overwrite IfSourceNewer
4. That will give them exactly the same effect as their sync, but it will start copying sooner, and will use less memory. This requires AzCopy 10.3.4 (earlier versions don't support it). 
   1. One day, we might optimize sync's memory usage. but that probably won't be any time soon.
  
## Recommended Documents

1. [AzCopy v10 TSG](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10)
