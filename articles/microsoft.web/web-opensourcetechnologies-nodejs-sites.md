<properties
	pageTitle="open source technologies/node.js"
	description="open source technologies/node.js"
	service="microsoft.web"
	resource="sites"
	authors="cts-shrahman, cts-shrahman"
    ms.author="shrahman,toan"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32444082"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public, MoonCake"
	articleId="7ba0fd5f-8a79-441e-8375-417e68b0b8fb"
/>

# open source technologies/node.js

## **Recommended documents**
Troubleshoot 500 errors or Availability issues:<br>
* [Best Practices and Troubleshooting Guide](https://docs.microsoft.com/azure/app-service/app-service-web-nodejs-best-practices-and-troubleshoot-guide)<br>
<br>

Addressing Slow Performance: <br>
	- Increase number of node.exe's per instance <br>
	- Disable Session Affinity (Sharing load with all serves equally) <br>
	- Check if issue is due to third-party services/database transactions. <br>
	- Use Browser Cache <br>
	- Serve Static files at IIS level/ Use CDN <br>
<br>
Deployment Errors: <br>
Check for error in deployment logs available at D:\home\site\deployment <br>
 - Instructions to [install native modules](https://prashanthmadi.github.io/2017/02/10/installing-native-nodejs-moduleson-azure-app-services-during-git-deployment-new.html) <br>
 - For general questions on how to [run different tasks during deployment](https://prashanthmadi.github.io/2016/07/31/azure-custom-deployment-new.html) <br>

Development Questions: <br>
 - [Nodejs App request Architecture](https://prashanthmadi.github.io/2016/11/07/nodejs-app-architecture-azure-app-services-windows-new.html)  <br>
 - [Nodejs and NPM Versions](https://prashanthmadi.github.io/2016/07/25/nodejs-npm-versions-azure-webaps-new.html) <br>

 Step-by-Step instructions for 

[Running Sample Nodejs App on Azure App Services](https://blogs.msdn.microsoft.com/azureossds/2016/04/18/sample-nodejs-app-on-azure-app-services/)<br>
[Running Meanjs on Azure App Services](https://prashanthmadi.github.io/2017/01/13/running-mean-js-app-on-azure-app-services-new.html)
* [Running Angularjs App on Azure App Services](https://prashanthmadi.github.io/2017/01/13/running-angular2-app-on-azure-app-services-with-ci-cd-new.html)
* [Running Ghost Blog on Azure App Services](https://prashanthmadi.github.io/2017/02/15/parse-on-azure-new.html)<br>
[Running Parse Server on Azure App Services](https://prashanthmadi.github.io/2017/02/15/parse-on-azure-new.html)<br>
[Running React + nodejs on Azure App Services](https://blogs.msdn.microsoft.com/reactjsnodejsazure/2017/08/01/reactjs-nodejs-express-azure-web-app/)<br>
