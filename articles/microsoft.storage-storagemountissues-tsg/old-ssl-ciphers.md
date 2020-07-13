<properties pageTitle="Old SSL Ciphers"
            description="Old SSL Ciphers"
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
            articleId="6401d380-ba65-4596-a1b1-45d0e4b67646"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Old SSL Ciphers

**Symptom**

If the customer is using .Net application to connect to azure file share and he is receiving the error:

**'Unhandled Exception: Microsoft.WindowsAzure.Storage.StorageException: The underlying connection was closed: An unexpected error occurred on a receive. ---> System.Net.WebException: The underlying connection was closed: An unexpected error occurred on a receive. ---> System.ComponentModel.Win32Exception: The client and server cannot communicate, because they do not possess a common algorithm'.**

**Cause**

The cause, is related to the removal of old SSL ciphers e.g. SSL3, TLS1.0, TLS1.1 and the fact that for TLS1.2 you have to opt-in by adding the following code before making any calls over a secure connection to the custom .Net application config file : System.Net.ServicePointManager.SecurityProtocol = System.Net.SecurityProtocolType.Tls12;

**Resolution**

For the client to negotiate TLS 1.2, the OS and the .NET Framework version both need to support TLS 1.2. The following sample shows how to enable TLS 1.2 in your .NET client.

```csharp
static void EnableTls12() 

{ 

 // Enable TLS 1.2 before connecting to Azure Storage 

System.Net.ServicePointManager.SecurityProtocol = System.Net.SecurityProtocolType.Tls12; 

// Connect to Azure Storage 

CloudStorageAccount storageAccount = CloudStorageAccount.Parse('DefaultEndpointsProtocol=https;AccountName={yourstorageaccount};AccountKey={yourstorageaccountkey};EndpointSuffix=core.windows.net'); 

 CloudBlobClient blobClient = storageAccount.CreateCloudBlobClient(); 

 CloudBlobContainer container = blobClient.GetContainerReference('foo'); 

 container.CreateIfNotExists(); 

 }
```

**Recommended Documents**

[https://docs.microsoft.com/azure/storage/common/storage-security-tls#enable-tls-12-in-net-client](https://docs.microsoft.com/azure/storage/common/storage-security-tls#enable-tls-12-in-net-client)

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->