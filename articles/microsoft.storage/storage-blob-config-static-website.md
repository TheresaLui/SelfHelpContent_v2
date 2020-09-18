<properties
	pageTitle="How to configure a Static Website"
	description="How to configure a Static Website"
	service="microsoft.storage"
	resource="storage"
	authors="passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32613339"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="9b2a8734-2db5-4b2b-899f-982f2edf3654"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Troubleshoot and resolve issues with Azure Static Websites

## **Recommended Steps**

Most customers resolved their Static Website issues, on their own, using the steps below.

### **Does storage firewall work with Static Website?**

The storage account has a built in [**firewall**](https://docs.microsoft.com/azure/storage/common/storage-network-security) feature available, but this will not affect the public [**web**](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website) endpoint. However enabling firewall restrict access to the other storage endpoints like blobs, files, dfs, table and queue.

### **Does Static Website support Azure AD?**

Currently Static Website doesn't support Azure AD authentication. There is no option to use social IDPs like Google Auth or Facebook using OpenID.

### **How to use custom domain with Static Website?**

Currently the way to configure [**custom domain**](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website-custom-domain#enable-custom-domain-and-ssl) with Static Website is to use [**Azure CDN**](https://docs.microsoft.com/azure/storage/blobs/storage-https-custom-domain-cdn). CDN provides consistent low latencies to your website from anywhere in the world. While CDN comes at an additional cost we have made it a compelling option with the removal of storage egress cost.

### **How to use custom SSL certificate with Static Website?**

Currently the way to configure [**custom SSL**](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website-custom-domain#enable-custom-domain-and-ssl) certificate with Static Website is to use [**Azure CDN**](https://docs.microsoft.com/azure/storage/blobs/storage-https-custom-domain-cdn). CDN provides consistent low latencies to your website from anywhere in the world. While CDN comes at an additional cost, we have made it a compelling option with the removal of storage egress cost.

### **How to add Custom headers and rules with Static Website?**

Currently the way to configure Host header with Static Website is to use [**Azure CDN - Verizon Premium**](https://docs.microsoft.com/azure/cdn/cdn-verizon-premium-rules-engine) on top of Azure Blob using Rules engine and access the CDN end point.Please provide us you feedback [**here**](https://feedback.azure.com/forums/217298-storage/suggestions/34959124-allow-adding-headers-to-static-website-hosting-in)

### **Why am I getting 404 from Static Website?**

Some of the common causes of getting an HTTP 404 error are as below
* Use the web endpoint like https://myaccount.z5.web.core.windows.net/index.html endpoint instead of the blob endpoint https://myaccount.blob.core.windows.net/$web/index.html . You can find the actual endpoint on the Azure portal.
* For Static Website file names along with extensions are case sensitive even though served over HTTP, therefore index.html != Index.html.
* CDN endpoint might take time to provision. Please wait till 90 mins after you provisioned new CDN for the propagation to happen.

### **Why is Root not redirecting to the page set for "index document name"?**

Ensure the name and extension as set in the file name on portal is the exact same of the file in the $web container including case sensitivity. For Static Website file names along with extensions are case sensitive even though served over HTTP, therefore index.html != Index.html.

## **Recommended Documents**

- [Static website hosting in Azure Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website)<br>
- [Quickstart steps to host a static website](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website#quickstart)<br>
- [CDN and SSL support for static website](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website#cdn-and-ssl-support)<br>
- [Custom domain names](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website#custom-domain-names)
