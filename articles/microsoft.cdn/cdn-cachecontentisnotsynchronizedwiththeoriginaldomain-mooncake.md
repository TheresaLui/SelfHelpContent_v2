<properties
    pageTitle="CDN cache content is not synchronized with the original domain"
    description="CDN cache content is not synchronized with the original domain"
    service="microsoft.cdn"
    resource="profiles"
    authors="huaiyizhu"
    displayOrder="8"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="cdnakamai, cdnverizon"
    productPesIds=""
    cloudEnvironments="Mooncake"
	articleId="afea129c-601d-4851-8d10-7fc51aa8ac2e"
	ownershipId="CloudNet_ContentDeliveryNetwork"
/>

# CDN cache content is not synchronized with the original domain

## **Recommended steps**
1. One possible cause is CDN caching rules are different from that of origin domain. Please refer to step 2. Or, CDN failed to cache the latest files origin domain updated. Please refer to step 5.

2. Please review cache rules. Click Manage button of CDN Profile page in [Azure portal](https://portal.azure.cn) to open CDN management page. Click "Domain Name Management" in the left navigation pane to select the domain name you'd like to review. Check if cache rules are consistent with that of the origin domain from pop-up sidebar on the right. If yes, please follow step 3 to 5. If no, please modify the cache rules and refer to step 5.

3. You can use wget, curl or browser developer tools to obtain information of "content-length" , "Last-modified" and "Content-MD5" fields for CDN cache and original domain.

4. If the above fields are consistent, then CDN cache content is synchronized with the original domain.

5. If the above fields are inconsistent, click Manage button of CDN Profile page in [Azure portal](https://portal.azure.cn) to open CDN management page. Click **Content Management** → **Cache refresh** → **Submit cache refresh** to perform a manual refresh of the file or directory. After the request is completed, follow step 3 to compare the above fields until CDN cache content is synchronized with the original domain.

Please click [here](https://docs.azure.cn/cdn/cdn-management-v2-portal-how-to-use) to see user guide for Azure CDN management portal.