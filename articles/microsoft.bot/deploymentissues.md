<properties
	pageTitle="Common Deployment Issues"
	description="Common Deployment Issues"
	service="Microsoft.BotService"
	resource="botServices"
	authors="JawaharGaneshS,meetshamir"
	ms.author="v-micric,jaws,stgum,saziz"
	displayOrder="103"
	selfHelpType="resource"
	supportTopicIds="32688661,32688636,32688637"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="A48F831F-F251-40B5-A602-09BA97C2381C"
	ownershipId="Compute_BotService"
/>
# Common Deployment Issues

## **Recommended Steps**

* Test to see if "Test in Web Chat" works from Azure Portal > Your Resource Group > Your Bot > Test in Web Chat

  * If it works, your deployment was successful and you need to troubleshoot why your client cannot connect to your deployed bot
  * If it doesn't work, please follow additional troubleshooting steps from this document

* If you ran into errors while executing deployment CLI commands, ensure you have the latest version of [Azure CLI](https://docs.microsoft.com/cli/azure/install-azure-cli?view=azure-cli-latest)
* Some CLI commands will fail without much explanation. This is usually a formatting error. For your CLI commands, ensure that:

	* The entire command has appropriate spacing
	* User-provided strings are surrounded by quotes
	* User-provided strings for resource names are free of special characters (this mostly applies to App Service Plan names). See [Naming rules and restrictions](https://docs.microsoft.com/azure/architecture/best-practices/resource-naming) for specific details.
	
* Ensure that you ran [the `az bot prepare-deploy` step](https://docs.microsoft.com/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0&tabs=csharp#51-retrieve-or-create-necessary-iiskudu-files) prior to deployment. Missing this step often manifests in a bot not starting or 404 errors (due to missing/incorrect `web.config`) when visiting `https://<yourBot>.azurewebsites.net`.
* Ensure that the file/folder structure of `https://<yourBot>.scm.azurewebsites.net/dev/wwwroot/` looks similar to your local bot. For Node bots, it will look mostly the same as your local bot files. For C# bots, it will have a lot of `Microsoft.*.dll` files along with `<yourBot>.dll`. All deployed bots should have a `web.config` file.
* For Node bots, you also need to have `node_modules` and `.env` deployed. For C# bots, you need `appsettings.json`. If your bot is missing `.env` or `appsettings.json` you need to either upload it, or copy the appropriate keys and values in `Azure Portal > Your Resource Group > Your App Service > Configuration`.
* Expanding on [the code deployment step](https://docs.microsoft.com/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0&tabs=csharp#52-zip-up-the-code-directory-manually): When deploying, zip the **contents** of your project folder and **not** the folder by itself. Your zip file should have the structure `code.zip/[each project file and folder]` and **not** `code.zip/myBot/[each project file and folder]`.
* Ensure that the MicrosoftAppId and MicrosoftAppPassword that you have in `appsettings.json`/`.env`/`App Service Configuration` matches the ones found in your [App Registration](https://ms.portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade)
* Ensure that your App Registration can be accessed by "Accounts in any organizational directory" by following [these steps](https://github.com/microsoft/BotBuilder-Samples/issues/1366#issuecomment-479087524).
* Go to `https://<yourBot>.scm.azurewebsites.net/dev/wwwroot/:output`, click Run, and see if any errors present themselves in the Output window

## **Recommended Documents**

* [Deploy your bot](https://docs.microsoft.com/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0)
* For Virtual Assistants and Skills: [Manual Deployment](https://microsoft.github.io/botframework-solutions/virtual-assistant/tutorials/deploy-assistant/cli/1-intro/#subcategory2_3)
* [Set up continuous deployment](https://docs.microsoft.com/azure/bot-service/bot-service-build-continuous-deployment?view=azure-bot-service-4.0)
