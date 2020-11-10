<properties
	pageTitle="Restore a Bot"
	description="Restore a Bot"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-anravi,saziz"
	displayOrder="190"
	selfHelpType="resource"
	supportTopicIds="32688658"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="0E06234B-81EE-4E83-890A-48DA573FA3DA"
	ownershipId="Compute_BotService"
/>
# Restore a Bot

## **Recommended Steps**

It is not possible to restore a bot on Azure if accidentally deleted. Once the Web App Bot is deleted, it is permanent and cannot to reversed.
A good practice is to always backup all the source code/configuration files in a repo like GitHub or your local machine so that you can redeploy the bot. Having a back up on cloud makes it easier to download them to your local machine and make the necessary changes to be able to deploy the bot again on Azure.

### Back up the bot files

1. Login to Azure and click on the Web App Bot you want to backup
2. Click on 'Build' under the Bot Management section on the left panel
3. Click on Download Bot source code link in the right-pane
4. Follow the prompts to download the code, and then unzip the folder. When downloading your bot, you will be given the option to include the settings (containing the keys and secrets) for your bot in your download, which may be necessary for your bot to work. If you choose Yes, the appsettings.json or .env file will have the keys.
5. The next step would be to either save your bot files in a designated folder on your local machine or upload them on [GitHub](https://help.github.com/en/github/importing-your-projects-to-github/adding-an-existing-project-to-github-using-the-command-line)

### Steps to Redeploy the Bot

If you have deleted your bot on Azure accidentally, you can still redeploy your most updated bot code downloaded on your local machine or from a repo. If you have your files on an online file storage, then you can download your bot files to your local machine for redeployment.

Refer to the link below for the steps to deploy your bot to Azure.

## **Recommended Documents**

* [Deploy your bot](https://docs.microsoft.com/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0&tabs=csharp)
