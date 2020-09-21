<properties
	pageTitle="How to check the version of AzCopy the customer is using"
	description="How to check the version of AzCopy the customer is using"
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
	articleId="a03dc636-3ac2-43e7-842a-381b1a50b526"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check the version of AzCopy the customer is using

**AzCopy** is a command-line utility that you can use to copy blobs or files to or from a storage account. **AzCopy V10(10.1.x)** is the currently supported version of **AzCopy**.

1. Enter 'azcopy' at the command prompt to expose version. 
2. C:\Users\janedoe\Downloads\azcopy_windows_amd64_10.1.2>azcopy
AzCopy 10.1.2
3. Alternatively, you can confirm in DGrep logs from the storage stamp FE in the "UserAgent" column. **[XSTORE->FrontEndSummaryPerfLogs](https://jarvis-west.dc.ad.msft.net/7A3558B2)**
    1. **EG. "UserAgent":"'''AzCopy/7.3.0'''**

