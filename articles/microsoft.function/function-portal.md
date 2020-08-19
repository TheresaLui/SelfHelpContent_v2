<properties
	pageTitle="Portal Issues"
	description="Portal Issues"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman, cts-shrahman"
    ms.author="shrahman,jebrook"
	displayOrder="12"
	selfHelpType="generic"
	supportTopicIds="32518045"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="cda73f84-a775-4414-a902-3cfda0b67eed"
	ownershipId="Compute_AppService"
/>

# Portal Issues

## **Recommended Steps**

The Azure Function Portal UX relies on specific outbound calls to a set of resources including the web app *funcationappname.azurewebsites.net*, Kudu *functionappname.scm.azurewebsites.net*, and other Azure Management APIs. If these calls are blocked or do not return a 200, the portal may not load completely. <br>

**Internal Load Balanced App Service Environments (ILB ASE) and Azure Functions**<br>

If the Function app is being created in an ILB ASE there are some required dependencies. Please see this [blog](https://blogs.msdn.microsoft.com/mihansen/2018/03/15/private-function-apps-in-azure-government-using-app-service-environment-ase/) for more detail on configuring Function Apps with ILB  ASEs. Common issues include the following list: <br>

1. Your VM is not on the virtual network, e.g. you are trying to do this from your laptop
2. The DNS entries are missing either from your hosts file or your DNS server if you have a DNS server on the virtual network
3. The SSL certificate is not trusted
4. The portal functions site is not listed in the CORS rules of your Function App: Navigate to the Kudu site of your function app (functionappname.scm.ilbdomain) and log in using the site level credentials available from the Publishing Profile of your function app.<br>

## **Recommended Documents**

* [Runtime Limitations](https://github.com/projectkudu/kudu/wiki/Azure-Web-App-sandbox)<br>
* [Known Issues](https://github.com/Azure/app-service-announcements/issues)
