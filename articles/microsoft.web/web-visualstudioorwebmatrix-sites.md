<properties
	pageTitle="deployment/visual studio"
	description="deployment/visual studio"
	service="microsoft.web"
	resource="sites"
	authors="cts-shrahman, cts-shrahman"
    ms.author="shrahman,benperk"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32588774"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="c7ffee97-9ae2-4870-8788-cd7c2534574a"
	ownershipId="Compute_AppService"
/>

# Visual studio 

## **Recommended Steps**

To resolve the most common issues with Visual Studio deployments via Web Deploy, try one or more of the following methods:

1. Make sure that you have the [latest version of the Azure SDK](https://azure.microsoft.com/downloads) for the version of Visual Studio that you are using
2. If using Deployment credentials, make sure that: <br>

	* The account is not disabled in Azure Active Directory
	* The user account format is correct (User account should NOT be preceded by the web app name NOR by a $)
	* The password is correct
	
	For more information see: [Wiki on Deployment Credentials](https://github.com/projectkudu/kudu/wiki/Deployment-credentials) <br>
	
3. If using Publishing credentials make sure that you download the most [recent publishing profile](https://github.com/projectkudu/kudu/wiki/Deployment-credentials) and that the user name is preceded by $
4. By default, when deploying to Azure App Service Web Apps, it will try to connect to the SCM site of your Web App http://(YourWebAppName).scm.azurewebsites.net. Make sure that Visual Studio is able to connect to it. <br>
5. If behind a proxy, make sure that Visual Studio is correctly [configured to use your proxy server](https://msdn.microsoft.com/library/dn771556.aspx)

## **Recommended Documents**

* [Web Deploy error codes](https://docs.microsoft.com/iis/publish/troubleshooting-web-deploy/web-deploy-error-codes) <br>

   * [ERROR_COULD_NOT_CONNECT_TO_REMOTESVC](https://docs.microsoft.com/iis/publish/troubleshooting-web-deploy/web-deploy-error-codes#errorcouldnotconnecttoremotesvc) <br>
   * [ERROR_DESTINATION_INVALID](https://docs.microsoft.com/iis/publish/troubleshooting-web-deploy/web-deploy-error-codes#errordestinationinvalid) <br>
   * [ERROR_INSUFFICIENT_ACCESS_TO_SITE_FOLDER](https://docs.microsoft.com/iis/publish/troubleshooting-web-deploy/web-deploy-error-codes#errorinsufficientaccesstositefolder) <br>
   * [ERROR_FILE_IN_USE](https://docs.microsoft.com/iis/publish/troubleshooting-web-deploy/web-deploy-error-codes#errorfileinuse) <br>

* [Dealing with locked files during deployment](https://github.com/projectkudu/kudu/wiki/Dealing-with-locked-files-during-deployment)  (*.lock files) <br>
* [Publish a Web app to Azure App Service using Visual Studio](https://docs.microsoft.com/visualstudio/deployment/quickstart-deploy-to-azure?view=vs-2017) <br>
* Deploying behind a proxy? [Proxy Authorization Required](https://azure.microsoft.com/blog/web-deploy-3-6-beta-released/)<br>
* [Make sure site correctly deploys locally](https://github.com/projectkudu/kudu/wiki/Make-sure-site-correctly-deploys-locally) <br>
* [Deployment FAQs](https://docs.microsoft.com/azure/app-service/faq-deployment) <br>
* [Deployment vs runtime issues](https://github.com/projectkudu/kudu/wiki/Deployment-vs-runtime-issues) <br>
* [How to create and deploy a simple ASP.NET MVC web project by using Visual Studio and Web Deploy](https://azure.microsoft.com/documentation/articles/web-sites-dotnet-get-started/)<br>
* [ASP.NET Web Deployment using Visual Studio - 12-part tutorial series that covers complete range of deployment tasks](http://www.asp.net/mvc/overview/deployment/visual-studio-web-deployment/introduction)<br>
* [How to Deploy Azure WebJobs using Visual Studio.](https://azure.microsoft.com/documentation/articles/websites-dotnet-deploy-webjobs/)<br>
* [Deploy a Secure ASP.NET MVC 5 app with Membership, OAuth, and SQL Database to Web Apps.](https://azure.microsoft.com/documentation/articles/web-sites-dotnet-deploy-aspnet-mvc-app-membership-oauth-sql-database/)<br>
* [Troubleshooting Web Deploy](http://www.iis.net/learn/publish/troubleshooting-web-deploy)<br>
* [You receive an error message when you use the Web Deployment Tool (Web Deploy) as a delegated user over a remote IIS manager connection via the Web Management Service (WMSVC)](https://support.microsoft.com/kb/2023855)
