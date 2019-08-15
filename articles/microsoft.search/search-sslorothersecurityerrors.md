<properties
	pageTitle="Connectivity/SSL or other security errors"
	description="Connectivity/SSL or other security errors"
	service="microsoft.search"
	resource="searchservices"
	authors="mrcarter8"
	selfHelpType="resource"
	supportTopicIds="32681387"
	resourceTags=""
	productPesIds="15568"
	cloudEnvironments="public"
	articleId="search-sslorothersecurityerrors"
/>

# SSL or other security errors
These are some common sources of security errors when connectoring to your Azure Search service:

*Azure Search listens on HTTPS port 443. All connections to the Azure Search service are are encrypted using SSL/TLS 1.2.  Please be sure to use TLS v1.2 for SSL connections to your service.
*Make sure your search service URL uses HTTPS.  If your URL contains HTTP instead of HTTPS, a 502 Bad Gateway status code will be returned.
*If you see a 403 error code, Forbidden, please confirm that you are passing a valid API key for the operation you are trying to perform.  For example, you may be passing a query key when trying to update the definition of an index. 

## **Recommended documents**
[Security and data privacy in Azure Search](https://docs.microsoft.com/azure/search/search-security-overview#encrypted-transmission-and-storage) <br>
[HTTP status codes (Azure Search)](https://docs.microsoft.com/rest/api/searchservice/http-status-codes)
[Azure Search encryption using customer-managed keys in Azure Key Vault](https://docs.microsoft.com/azure/search/search-security-manage-encryption-keys)