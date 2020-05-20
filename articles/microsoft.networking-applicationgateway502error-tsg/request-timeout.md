<properties
	pageTitle="TSG Content Step: Check if the issue is a request time out"
  	description="TSG Content Step: Check if the issue is a request time out"
  	service="microsoft.network"
  	resource="applicationGateway"
  	authors="JRMayberry"
    ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="31a759a6-fdd7-440e-99f4-1afe52833288"
	ownershipId="CloudNet_AzureApplicationGateway"
/>


**How to check if the issue is caused by the request timeout setting:**

If at least one server is healthy, we can try increasing the request time-out, and check whether the problem is resolved. To verify, follow these steps:

1. Click on the Backend HTTP Settings Collection section of the Application Gateway in ASC
2. Select the **HTTP setting** that is configured in your rule. This can be identified by the Request Routing Rule Links column
3. The **Request Timeout** is measured in seconds. Suggest the customer to enter a value for request timeout in HTTP settings higher than how long the backend server takes to return the response to every request.
4. To verify if the timeout is happening, check the [AppGWT -> ReqResp](https://jarvis-west.dc.ad.msft.net/7D7EA793) in Jarvis Logs and for each request, the timeTaken value (in milliseconds) will point to the time taken for the whole request to be processed starting from the first byte received by the Application Gateway till the last byte sent out to the client. If the server is taking more time than this, the requests will be timed out.
5. To measure how long the server takes to respond, access the backend server on the same path and hostname directly by bypassing AppGW and measure the time in the browser developer tools (F12).
