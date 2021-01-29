<properties
	pageTitle="Upload / Download Specific Files with AzCopy "
	description="Upload / Download Specific Files with AzCopy "
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
	articleId="476f5f82-b20c-4235-99dc-6c515e7f7a24"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Upload / Download Specific Files with AzCopy 

1. You can create a list of specific files (or directories) to transfer, and then tell AzCopy to transfer only those exact files. 
2. **As of version 10.3, this flag remains undocumented (except for this wiki page) and it does not appear in the in-app command line help.**. 
3. It is however regularly used by Azure Storage Explorer to pass file lists to its embedded copy of AzCopy.
4. To use this feature, create a text file that lists the files to be transferred, which are all under the root source directory.

~~~shell

File_1.pdf
subdirA\File_2.pdf

~~~

5. Then, invoke AzCopy like this for uploads:

~~~shell

AzCopy copy d:\sourceDir "http://urlToDestination" --list-of-files fullPathToYourTextFile

~~~

6. And it will transfer the files **d:\sourceDir\File_1.pdf** and **d:\sourceDir\subdirA\File_2.pdf**
7. For downloads, the process is similar - the names in the file are appended to the source container/virtual directory to produce the full URLs of the files to download.
8. Note: you can also list directories as well as individual files. You should also add the --recursive flag to your command line in that case).

## How to Download a VHD 

When a disk is used for a VM the MD5 hash changes after usage on the disk alters the content of the blob, but does not update the MD5 hash. So when it's downloaded, you may get a hash mis-match. If you have such a blob, there is no way AzCopy can check the hash on download (because the hash is out of date and incorrect) so turn off the hash checking with `--check-md5 NoCheck`. The default is to check hashes for all blobs that have them, but to do no check on blobs that have no hash.? 

## Recommended Documents

1. [Listing Specific Files to Transfer](https://github.com/Azure/azure-storage-azcopy/wiki/Listing-specific-files-to-transfer) for more details.
2. [Download a VHD](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=how-to-download-a-vhd) 
