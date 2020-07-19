<properties
	pageTitle="Questions on Publishing code"
	description="Questions on Publishing code"
	service="microsoft.web"
	resource="sites"
	authors="sudhat"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32589282"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="30a2fd9a-a729-4fe3-92ae-9d585beff497"
	ownershipId="Compute_AppService"
/>
# Questions on Publishing code
## **Recommended documents** 
**FTP:**<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[How do I deploy my app to Azure App Service using FTP/FTPS?](https://docs.microsoft.com/azure/app-service-web/app-service-deploy-ftp)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[How to Deploy manually by uploading files with FTP](https://docs.microsoft.com/azure/app-service-web/web-sites-deploy?toc=%2fazure%2fapp-service%2ftoc.json#ftp)<br>
**Troubleshooting guidance for Git, GitHub, BitBucket, DropBox scenarios:**<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Investigating Continuous deployment issues](https://github.com/projectkudu/kudu/wiki/Investigating-continuous-deployment)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Local Git Deployment and troubleshooting](https://docs.microsoft.com/azure/app-service-web/app-service-deploy-local-git?toc=%2fazure%2fapp-service%2ftoc.json)<br>
**General Documentation for Continuous Deployment to Azure App Service:**<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Continuous Deployment to Azure App Service - GitHub / BitBucket / Dropbox Deployment](https://docs.microsoft.com/azure/app-service-web/app-service-continuous-deployment)<br>
**Troubleshooting issues with Visual Studio deployments:**<br>
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
5.	If behind a proxy, make sure that Visual Studio is correctly configured to use your proxy server. For more information see: [More info on Proxy Authorization Required Error](https://msdn.microsoft.com/library/dn771556.aspx) <br>
**ARM Template:**<br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[How do I automate Azure App Service WebApps using Powershell?](https://blogs.msdn.microsoft.com/puneetgupta/2016/03/21/automating-webapps-hosted-in-azure-app-service-through-powershell-arm-way/)<br>
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Reference - Descriptions and Syntax for Azure App service web apps cmdlets](https://docs.microsoft.com/powershell/module/azurerm.websites/?view=azurermps-4.3.1)<br>