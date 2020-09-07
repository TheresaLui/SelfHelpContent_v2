<properties
  	pageTitle="TSG Content Step: Check if there is a custom probe"
	description="TSG Content Step: Check if there is a custom probe"
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
	articleId="82af8570-2d65-4710-847a-7de2e1617468"
	ownershipId="CloudNet_AzureApplicationGateway"
/>

# How to check if there is a custom probe configured

Check the custom probe (Backend HTTP Settings --> HTTP Setting --> Probe) settings based on the error that you got in the backend health status

1. **TCP Connect error**: This error means that a TCP session could not be established. Check the port on HTTP settings and verify if you can connect to the server on the port or if any NSG/UDR is affecting the traffic.
2. **DNS resolution error**: Application gateway could not create a probe for this backend. This usually happens when the FQDN of the backend has not been entered correctly. Enter a resolvable FQDN or check your DNS settings.
3. Probe status code mismatch: Based on the received status code, check the probe parameters:

	* Received 401: Check if the backend server requires authentication. Application Gateway probes can’t pass credentials for authentication at this point. Either allow HTTP 401 in Probe status code match or probe to a path where it does not require authentication.
	* Received 403: Check if access to the path is allowed in the backend server
	* Received 404: Check hostname, path if it is accessible in the backend server. Change the hostname or path parameter to an accessible value.
	* Received 405: Check if the server allows HTTP Method GET
	* Received 500: Internal server error. Check the backend server's health and whether the services are running.
	* Received 503: Service unavailable. Check the backend server's health and whether the services are running.

4. HTTP response body mismatch: Body of the backend's HTTP response did not match the probe setting. If the response body for the probe doesn’t match with what’s configured in the Application Gateway, change the probe settings or check on the server’s response.
