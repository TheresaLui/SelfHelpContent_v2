<properties
	pageTitle="deployment/visual studio"
	description="deployment/visual studio"
	service="microsoft.web"
	resource="sites"
	authors="shrahman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32588774"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public"
/>

# Visual studio or Webmatrix Deployment

## **Recommended steps**

To resolve the most common issues with Visual Studio deployments via Web Deploy, try one or more of the following methods:

1.	Make sure that you have the latest version of the Azure SDK for the version of Visual Studio that you are using: [Download Location.](https://azure.microsoft.com/downloads) <br>
2.	If using Deployment credentials, make sure that: <br>
	a. The account is not disabled in Azure Active Directory. <br>
	b. The user account format is correct (User account should NOT be preceded by the web app name NOR by a $). <br>
	c. The password is correct. <br>
For more information see: [Wiki on Deployment Credentials](https://github.com/projectkudu/kudu/wiki/Deployment-credentials) <br>
3.	If using Publishing credentials make sure that: <br>
	a. You download the most recent publishing profile and that the user name is preceded by $. For more information please review the: [Deployment credentials Wiki](https://github.com/projectkudu/kudu/wiki/Deployment-credentials).<br>
4.	By default, when deploying to Azure App Service Web Apps, it will try to connect to the SCM site of your Web App (http://<yourWebAppName>.scm.azurewebsites.net). Make sure that Visual Studio is able to connect to it. <br>
5.	If behind a proxy, make sure that Visual Studio is correctly configured to use your proxy server. For more information see: [More info on Proxy Authorization Required Error](https://msdn.microsoft.com/library/dn771556.aspx)

## **Recommended documents**
[How to create and deploy a simple ASP.NET MVC web project by using Visual Studio and Web Deploy](https://azure.microsoft.com/documentation/articles/web-sites-dotnet-get-started/)<br>
[ASP.NET Web Deployment using Visual Studio - 12-part tutorial series that covers complete range of deployment tasks](http://www.asp.net/mvc/overview/deployment/visual-studio-web-deployment/introduction)<br>
[Build and Deploy Azure Web Apps using Team Foundation Server/Services](https://blogs.msdn.microsoft.com/tfssetup/2016/04/01/build-and-deploy-azure-web-apps-using-team-foundation-serverservices-vnext-builds/)<br>
[How to Deploy Azure WebJobs using Visual Studio.](https://azure.microsoft.com/documentation/articles/websites-dotnet-deploy-webjobs/)<br>
[Deploy a Secure ASP.NET MVC 5 app with Membership, OAuth, and SQL Database to Web Apps.](https://azure.microsoft.com/documentation/articles/web-sites-dotnet-deploy-aspnet-mvc-app-membership-oauth-sql-database/)<br>
[Troubleshooting Web Deploy](http://www.iis.net/learn/publish/troubleshooting-web-deploy)<br>
[You receive an error message when you use the Web Deployment Tool (Web Deploy) as a delegated user over a remote IIS manager connection via the Web Management Service (WMSVC)](https://support.microsoft.com/kb/2023855)
