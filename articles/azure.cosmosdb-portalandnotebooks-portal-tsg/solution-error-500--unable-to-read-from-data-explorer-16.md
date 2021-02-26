<properties
	  pageTitle="Error 500: Unable to Read from Data Explorer"
	  description="Error 500: Unable to Read from Data Explorer"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="7be9cf7e-1031-4a04-8b64-edc1f32d4f93"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Error 500: Unable to Read from Data Explorer

<!--issueDescription-->

Dear customer,

One possible cause if you are using the SDK used by the application is .Net SDK which created Json Document. But Mongo is based on bson document. This mismatch would generate error in the portal.  However, the portal would fail to parse since its trying to use the mongo protcol to read the data.
 
Collect Information for investigation

#### How to Collect Fiddler Traces:

Please install the fiddler from the web
https://www.telerik.com/download/fiddler

1.Fiddler SSL Setting
- Click Tools Options 
- Click Https Tab
- Ensure the following setting is configured, see [Image Setting](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EVLECLcFBb9GnfBE32t_HckBCitPBlvfOyx9XbyvdMVC1w?e=axfcms). 

2. Close the Fiddler
3. Open the Fiddler
4. Start the Collection
- Click File Menu
- Click Capture Trace
5. Stop the Collection
- Click File Menu
- Click Capture Trace
6. Save the Trace
- Click File Menu
- Save -> All Session
- Input the file name
 
**Example Fiddler Trace below showing error events:**

```
Response Tab  
HTTP/1.1 500 Internal Server Error  
Cache-Control: no-cache  
Pragma: no-cache  
Content-Length: 153  
Content-Type: text/plain; charset=utf-8  
Expires: -1  
Server: Microsoft-IIS/10.0  
Set-Cookie: browserId=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx; domain=portal-prod-centralus-mongo.portal-prod-centralus.p.azurewebsites.net; path=/; secure; HttpOnly  
x-content-type-options: nosniff  
X-XSS-Protection: 1; mode=block  
x-ms-version: 5.0.302.970 (production_sdk#4681e966b1.180116-1257)  
Strict-Transport-Security: max-age=31536000; includeSubDomains  
Access-Control-Allow-Origin: https://main.documentdb.ext.azure.com  
Access-Control-Allow-Credentials: true  
Access-Control-Expose-Headers: x-ms-request-charge,x-ms-continuation  
X-Content-Type-Options: nosniff  
X-UA-Compatible: IE=edge  
Strict-Transport-Security: max-age=31536000; includeSubDomains  
Set-Cookie: ARRAffinity=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx;Path=/;HttpOnly;Domain=portal-prod-centralus-mongo.portal-prod-centralus.p.azurewebsites.net

Date: Tue, 27 Mar 2018 22:21:02 GMT
```

Thank you.

<!--/issueDescription-->

