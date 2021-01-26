<properties
	pageTitle="Troubleshoot and resolve Azure Storage authentication issues with SAS token"
	description="Troubleshoot and resolve Azure Storage authentication issues with SAS token"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="annayak"
	ms.author="annayak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32678713,32679283,32679297,32679290"
	resourceTags=""
	productPesIds="15629,16459,16461,16462,16598"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="8f25d274-c9e8-48ef-a590-3dad80217745"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Troubleshoot and resolve Azure Storage access issues with Shared Access Signature (SAS) Token

## **Recommended Steps** 

Most customers can resolve their SAS token authentication and connectivity issues by using the following steps.

### **Shared Access Signature (SAS)**

- [When to use Shared Access Signature (SAS) tokens?](https://docs.microsoft.com/azure/storage/storage-dotnet-shared-access-signature-part-1#when-should-you-use-a-shared-access-signature)
- [Delegating Access with a Shared Access Signature](https://docs.microsoft.com/rest/api/storageservices/fileservices/delegating-access-with-a-shared-access-signature)
- [Using SAS with Storage Explorer](https://docs.microsoft.com/azure/vs-azure-tools-storage-manage-with-storage-explorer#attach-storage-account-using-sas)
- [Authorization options for Azure Storage Services](https://docs.microsoft.com/rest/api/storageservices/authorization-for-the-azure-storage-services)
- [Best practices when using SAS](https://docs.microsoft.com/azure/storage/common/storage-dotnet-shared-access-signature-part-1#best-practices-when-using-sas)

### **ADLSGen2 - SAS with Directory Scoped Access**
- [Service SAS support for Directory scoped access](https://docs.microsoft.com/rest/api/storageservices/create-service-sas#service-sas-support-for-directory-scoped-access)

### **Common SAS Errors**  

**Receiving HTTP 403 (Forbidden) messages** 
  
**Note:** If an expired SAS key is the cause, you will not see any entries in the server-side Storage Logging log data.

If your client application is throwing HTTP 403 (Forbidden) errors, the most likely causes are as follows:

1. Client is using an expired SAS token
2. Clock skew 
3. Invalid keys 
4. Empty headers

To resolve these issues, try these steps:

* Typically, you should not set a start time when you create a SAS for a client to use immediately. If there are small clock differences between the host generating the SAS using the current time and the storage service, it's possible for the storage service to receive a SAS that is not yet valid.
* Don't set a very short expiration time on a SAS. Again, small clock differences between the host generating the SAS and the storage service can lead to a SAS expiring earlier than anticipated.
* Does the version parameter in the SAS key (for example, sv=2015-04-05) match the version of the Storage Client Library you are using? We recommend that you always use the latest version of the Storage Client Library.
* If you regenerate your storage access keys, any existing SAS tokens may be invalidated. This issue may arise if you generate SAS tokens with a long expiration time for client applications to cache.    
       
## **Recommended Documents**

* [Logging with .NET Storage Client Library](https://docs.microsoft.com/rest/api/storageservices/client-side-logging-with-the-.net-storage-client-library)<br>
* [Logging with Java Storage Client Library](https://docs.microsoft.com/rest/api/storageservices/client-side-logging-with-the-microsoft-azure-storage-sdk-for-java)<br>
* [Sample client library log generated for HTTP 403 issues](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting?#the-client-is-receiving-403-messages)

### **Receiving HTTP 404 (Not found) messages**
  
If your client application is receiving an HTTP 404 (Not found) message from the server, this implies that the object the client was attempting to use (such as an entity, table, blob, container, or queue) does not exist in the storage service.

The most likely reasons for this are:

1. The client or another process previously deleted the object
2. Shared Access Signature (SAS) authorization issue 
3. Client-side JavaScript code does not have permission to access the object 
4. Network failure and lost network packets can lead to the storage service returning HTTP 404 messages to the client

## **Recommended Documents**

* [Configure Storage Server Side Logging from Portal ](https://docs.microsoft.com/azure/storage/common/storage-monitor-storage-account#configure-logging)
* [Analyze Storage Server Side Logs](https://docs.microsoft.com/azure/storage/common/storage-analytics-logging)<br>
* [Logging with .NET Storage Client Library](https://docs.microsoft.com/rest/api/storageservices/client-side-logging-with-the-.net-storage-client-library)
* [Logging with Java Storage Client Library](https://docs.microsoft.com/rest/api/storageservices/client-side-logging-with-the-microsoft-azure-storage-sdk-for-java)<br>

The following links provide sample server and client-side logs for reference, as well as guidance on how to resolve these errors:

- [The client or another process previously deleted the object](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#client-previously-deleted-the-object)
- [Shared Access Signature (SAS) authorization issue](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#SAS-authorization-issue)
- [Client-side JavaScript code does not have permission to access the object](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#JavaScript-code-does-not-have-permission)
- [Network failure and lost network packets](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#network-failure)

### **Receiving HTTP 409 (Conflict) messages**

If your client application is receiving an HTTP 409 (Conflict) message from the server, this means that the server is processing a previous request on the same object which conflicts with the current request.

## **Recommended Documents**

* [Configure Storage Server Side Logging from Portal ](https://docs.microsoft.com/azure/storage/common/storage-monitor-storage-account#configure-logging)
* [Analyze Storage Server Side Logs](https://docs.microsoft.com/azure/storage/common/storage-analytics-logging)

The following link provides sample server side logs as reference and guidance on how to resolve these errors:

- [The client is receiving HTTP 409 (Conflict) messages](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-409-messages)

### **SAS Examples**

- [SAS Blob Examples](https://docs.microsoft.com/rest/api/storageservices/service-sas-examples#blob-examples)
- [SAS File Examples](https://docs.microsoft.com/rest/api/storageservices/service-sas-examples#file-examples)
- [SAS Table Examples](https://docs.microsoft.com/rest/api/storageservices/service-sas-examples#table-examples)
- [SAS Queue Examples](https://docs.microsoft.com/rest/api/storageservices/service-sas-examples#queue-examples)

### **Constructing SAS Token** 

- [How to construct Account SAS](https://docs.microsoft.com/rest/api/storageservices/fileservices/Constructing-an-Account-SAS?redirectedfrom=MSDN)
- [How to construct Service SAS](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas)
- [Specify Access Policy in the SAS Token](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas#specifying-the-access-policy)
- [Create SAS token with restricted permissions](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas#specifying-permissions)
- [Create SAS token accessible from specify IP address or IP range](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas#specifying-ip-address-or-ip-range)
- [Create SAS token accessible only over HTTPs](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas#specifying-the-http-protocol)
- [Create SAS token valid for a certain period](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas#specifying-the-signature-validity-interval) 
- [Create SAS token for only Blob Service](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas#specifying-the-signed-resource-blob-service-only)
- [Create SAS token for only File Service](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas#specifying-the-signed-resource-file-service-only)
- [Create SAS token for only Table Service](https://docs.microsoft.com/rest/api/storageservices/constructing-a-service-sas#specifying-the-table-name-table-service-only)
