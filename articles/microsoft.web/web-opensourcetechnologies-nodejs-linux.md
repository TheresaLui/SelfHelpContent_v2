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
	productPesIds="16170,16333"
	cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
	articleId="39263c39-9ac9-41a5-97bb-44b753878356"
	ownershipId="Compute_AppService"
/>

# open source technologies/node.js

## **Recommended Steps**

### Addressing Slow Performance

* Check if issue is due to third-party services/database transactions
* Use Browser Cache 
* Serve Static files / Use CDN 

### Deployment Errors

* Check for error in deployment logs available at /home/site/deployment or download using KUDU API by going to "https://<sitename>.scm.azurewebsites.net/api/dump"
* Instructions to [install native modules](https://prashanthmadi.github.io/2017/02/10/installing-native-nodejs-moduleson-azure-app-services-during-git-deployment-new.html) 
* For general questions on how to [run different tasks during deployment](https://prashanthmadi.github.io/2016/07/31/azure-custom-deployment-new.html)
	
### Development Questions

* [Nodejs App request Architecture](https://prashanthmadi.github.io/2016/11/07/nodejs-app-architecture-azure-app-services-windows-new.html) 
* [Nodejs and NPM Versions](https://prashanthmadi.github.io/2016/07/25/nodejs-npm-versions-azure-webaps-new.html)

### Step-by-Step instructions

* [Running Sample Nodejs App on Azure App Services](https://azureossd.github.io/2016/04/18/sample-nodejs-app-on-azure-app-services/)
* [Running Meanjs on Azure App Services](https://prashanthmadi.github.io/2017/01/13/running-mean-js-app-on-azure-app-services-new.html)
* [Running Angularjs App on Azure App Services](https://prashanthmadi.github.io/2017/01/13/running-angular2-app-on-azure-app-services-with-ci-cd-new.html)
* [Running Ghost Blog on Azure App Services](https://prashanthmadi.github.io/2017/02/15/parse-on-azure-new.html)
* [Running Parse Server on Azure App Services](https://prashanthmadi.github.io/2017/02/15/parse-on-azure-new.html)
