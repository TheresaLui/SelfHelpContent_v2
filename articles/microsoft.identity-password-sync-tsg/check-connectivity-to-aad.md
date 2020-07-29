<properties
	pageTitle="Check connectivity to AAD"
	description="Check connectivity to AAD"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ed98dda7-b21a-4a0c-aeac-8576868c40e3"
/>

# How to check connectivity to AAD

* To verify if the Azure AD Connect server has actual connectivity with the Proxy and Internet, use some PowerShell like below

~~~powershell

Invoke-WebRequest -Uri https://adminwebservice.microsoftonline.com/ProvisioningService.svc

~~~

* PowerShell uses the configuration in machine.config to contact the proxy. 
* The settings in winhttp/netsh should not impact these cmdlets.
* If the proxy is correctly configured, you should get a success status (200)
* If you receive Unable to connect to the remote server, then PowerShell is trying to make a direct call without using the proxy or DNS is not correctly configured. Make sure the machine.config file is correctly configured. 
* If the proxy is not correctly configured, you get an error as follows
   * Forbidden (403)
   * Proxy Authentication Request (407)

## **Recommended Documents**

* [Troubleshoot connect connectivity](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/tshoot-connect-connectivity)
* [Azure AD Connect: ADConnectivityTools PowerShell Reference](https://docs.microsoft.com/en-us/azure/active-directory/hybrid/reference-connect-adconnectivitytools)
* [Azure AD Connect Network and Name Resolution Prerequistes Test](https://gallery.technet.microsoft.com/scriptcenter/Azure-AD-Connect-Network-150c20a3)
