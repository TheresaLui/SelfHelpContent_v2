<properties
  pagetitle="Troubleshoot and resolve issues with Azure Static Websites&#xD;"
  service="microsoft.storage"
  resource="storage"
  ms.author="passap,broder"
  selfhelptype="Generic"
  supporttopicids="32613339"
  resourcetags=""
  productpesids="16459"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="9b2a8734-2db5-4b2b-899f-982f2edf3654"
  ownershipid="StorageMediaEdge_StorageBlobs" />
# Troubleshoot and resolve issues with Azure Static Websites

## **Recommended Steps**

Most users can resolve issues with Static Website by using the following steps.

### **Does storage firewall work with Static Website?**

The storage account has a built-in [**firewall feature**](https://docs.microsoft.com/azure/storage/common/storage-network-security) available, but this does not affect the [**public web**](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website) endpoint. It does enable firewall restrict access to other storage endpoints, such as blobs, files, dfs, tables, and queues.

### **Does Static Website support Azure AD?**

Currently, Static Website doesn't support Azure AD authentication. There is no option to use social IDPs, such as Google Auth or Facebook, using OpenID.

### **How do I use a custom domain with Static Website?**

Currently, you can configure a [**custom domain**](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website-custom-domain#enable-custom-domain-and-ssl) with a static website by using [**Azure CDN**](https://docs.microsoft.com/azure/storage/blobs/storage-https-custom-domain-cdn). CDN provides consistent low latencies to your website from anywhere in the world. Although CDN comes at an additional cost, we have removed the storage egress cost.

### **How do I use custom SSL certificate with a static website?**

Currently, you can configure a [**custom SSL**](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website-custom-domain#enable-custom-domain-and-ssl) certificate with a static website by using [**Azure CDN**](https://docs.microsoft.com/azure/storage/blobs/storage-https-custom-domain-cdn). CDN provides consistent low latencies to your website from anywhere in the world. Although CDN comes at an additional cost, we have removed the storage egress cost.

### **How do I add custom headers and rules with a static website?**

Currently, you can configure Host header with a static website by using [**Azure CDN - Verizon Premium**](https://docs.microsoft.com/azure/cdn/cdn-verizon-premium-rules-engine) on top of Azure Blob, using the Rules engine and accessig  the CDN end point. We'd be interested to hear your feedback [**here**](https://feedback.azure.com/forums/217298-storage/suggestions/34959124-allow-adding-headers-to-static-website-hosting-in).

### **Why am I getting an HTTP 404 error from a static website?**

Following are some of the common causes of getting an HTTP 404 error:
* Using a web endpoint such as https://myaccount.z5.web.core.windows.net/index.html instead of the blob endpoint https://myaccount.blob.core.windows.net/$web/index.html. You can find the actual endpoint on the Azure portal.
* File names and extensions in a static website are case-sensitive even though they're served over HTTP. For example, index.html != Index.html.
* The CDN endpoint can take some time to provision. Wait up to 90 minutes after you provision a new CDN for the propagation to complete.

### **Why is Root not redirecting to the page set for "index document name"?**

Ensure that the name and extension, as set in the file name on portal, are exactly the same as the file in the $web container, including case sensitivity. static website file names and extensions are case-sensitive even though they're served over HTTP. For example, index.html != Index.html.

## **Recommended Documents**

- [Static website hosting in Azure Storage](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website)<br>
- [Quickstart steps to host a static website](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website-how-to)<br>
- [CDN and SSL support for static website](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website#cdn-and-ssl-support)<br>
- [Custom domain names](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website#custom-domain-names)
