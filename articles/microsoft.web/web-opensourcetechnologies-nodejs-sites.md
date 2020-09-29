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
	cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
	articleId="7ba0fd5f-8a79-441e-8375-417e68b0b8fb"
	ownershipId="Compute_AppService"
/>

# open source technologies/node.js

## **Recommended Steps**

* Troubleshoot 500 errors or Availability issues: [Best Practices and Troubleshooting Guide](https://docs.microsoft.com/azure/app-service/app-service-web-nodejs-best-practices-and-troubleshoot-guide)

* Addressing Slow Performance: 

	- Increase number of node.exes per instance 
	* Disable Session Affinity (Sharing load with all serves equally) 
	* Check if issue is due to third-party services/database transactions
	* Use Browser Cache 
	* Serve Static files at IIS level/ Use CDN 
	
* Deployment Errors:

	* Check for error in deployment logs available at D:\home\site\deployment 
	* Instructions to [install native modules](https://prashanthmadi.github.io/2017/02/10/installing-native-nodejs-moduleson-azure-app-services-during-git-deployment-new.html) 
	* For general questions on how to [run different tasks during deployment](https://prashanthmadi.github.io/2016/07/31/azure-custom-deployment-new.html) <br>

* Development Questions: 

	* [Nodejs App request Architecture](https://prashanthmadi.github.io/2016/11/07/nodejs-app-architecture-azure-app-services-windows-new.html)
	* [Nodejs and NPM Versions](https://prashanthmadi.github.io/2016/07/25/nodejs-npm-versions-azure-webaps-new.html)

## **Recommended Documents**

* [Running Sample Nodejs App on Azure App Services](https://blogs.msdn.microsoft.com/azureossds/2016/04/18/sample-nodejs-app-on-azure-app-services/)
* [Running Meanjs on Azure App Services](https://prashanthmadi.github.io/2017/01/13/running-mean-js-app-on-azure-app-services-new.html)
* [Running Angularjs App on Azure App Services](https://prashanthmadi.github.io/2017/01/13/running-angular2-app-on-azure-app-services-with-ci-cd-new.html)
* [Running Ghost Blog on Azure App Services](https://prashanthmadi.github.io/2017/02/15/parse-on-azure-new.html)
* [Running Parse Server on Azure App Services](https://prashanthmadi.github.io/2017/02/15/parse-on-azure-new.html)
* [Running React + nodejs on Azure App Services](https://blogs.msdn.microsoft.com/reactjsnodejsazure/2017/08/01/reactjs-nodejs-express-azure-web-app/)
