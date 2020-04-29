<properties
	pageTitle="Troubleshoot continuous deployment"
	description="Troubleshoot continuous deployment"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-danava,jaws,cmullins,saziz"
	displayOrder="106"
	selfHelpType="resource"
	supportTopicIds="32688634"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="08453FC4-5CD4-480D-ADAE-D98EE49BB381"
	ownershipId="Compute_BotService"
/>
# Troubleshoot continuous deployment

## **Recommended Steps**

### **Getting continuous deployment working**

* Your bot must be deployed to Azure and you must have a App Service to be able to configure continuous deployment
* Ensure your repository has the [correct files](https://docs.microsoft.com/azure/bot-service/bot-service-build-continuous-deployment?view=azure-bot-service-4.0#prepare-your-repository)
* Ensure your repository is working as expected
* Using Azure DevOps or GitHub, your repository will have a .git folder and at least one branch
* Ensure logged in and shows correct account/org
* If you are not seeing any values in drop-downs (org/repo/branch) when configuring your connection, refresh the browser

### **Application no longer deploying**

* Check for errors showing in the App Service's Deployment Center. If so, review to understand what is now failing.
* Check to make sure the remote repository is still available
* Go to Deployment Center underneath App Service
* Click on the Repository link to have the repository open in another tab and ensure it is the correct one
* Click on sync button to attempt a new synchronization
* To isolate where the issue might be, you may consider creating a new App Service and configure deployment from there
* If that works, then it is an issue with the Configuration within the initial App Service
 * Follow directions [here](https://docs.microsoft.com/azure/bot-service/bot-service-build-continuous-deployment?view=azure-bot-service-4.0#disable-continuous-deployment) to disconnect and disable Continuous Deployment
 * Reconnect to repository to [re-enable continuous deployment](https://docs.microsoft.com/azure/bot-service/bot-service-build-continuous-deployment?view=azure-bot-service-4.0#continuous-deployment-using-github)

## **Recommended Documents**

* [Deploy your bot](https://docs.microsoft.com/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0)
* [Set up continuous deployment](https://docs.microsoft.com/azure/bot-service/bot-service-build-continuous-deployment?view=azure-bot-service-4.0)
