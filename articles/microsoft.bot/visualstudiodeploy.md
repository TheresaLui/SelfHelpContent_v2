<properties
	pageTitle="Deploy your C# bot using Visual Studio"
	description="Deploy your C# bot using Visual Studio"
	service="Microsoft.BotService"
	resource="botServices"
	authors="meetshamir"
	ms.author="v-jewail,huanchix,cmullins,saziz"
	displayOrder="105"
	selfHelpType="resource"
	supportTopicIds="32688663"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="AE0A4AB8-9453-421C-95BA-53019D458903"
	ownershipId="Compute_BotService"
/>
# Deploy your bot using Visual Studio

## **Recommended Steps**

Note: This topic is for the latest release of the SDK (v4). 

After you have created your bot and tested it locally, you can deploy it to Azure to make it accessible from anywhere. Deploying your bot to Azure will involve paying for the services you use. The billing and cost management article helps you understand Azure billing, monitor usage and costs, and manage your account and subscriptions.

In this article, we'll show you how to deploy a C# bot using Visual Studio and the Azure portal. It would be useful to read this article before following the steps, so that you fully understand what is involved in deploying a bot.

### **Deploy your bot in App Service**

You will first deploy the bot to Azure from Visual Studio in an App Service. Then you’ll configure your bot with the Azure Bot Service using Bot Channels Registration.

Note: If your Visual Studio project name has spaces, the deployment steps outlined below will not work.

1. In the Solution Explorer window, right click on your project’s node and select Publish  
2. In the Pick a publish target dialog, ensure App Service is selected on the left and Create New is selected on the right
3. Click the Publish button
4. In upper right of the dialog, ensure the dialog is showing the correct user ID for your Azure subscription
5. Enter App Name, Subscription, Resource Group, and Hosting Plan information
6. When ready, click Create. It can take a few minutes to complete the process
7. Once complete, a web browser will open showing your bot’s public URL
8. Make a copy of this URL (it will be something like https://.azurewebsites.net/)

Note: You’ll need to use the HTTPS version of the URL when registering your bot. Azure provides SSL support with Azure App Service.

### **Create your bot channel's registration**

With your bot deployed in Azure you need to register it with the Azure Bot Service:

1. Access the Azure Portal at https://portal.azure.com
2. Log in using the same identity you used earlier from Visual Studio to publish your bot
3. Click Create a resource
4. In the Search the Marketplace field type Bot Channels Registration and press Enter
5. In the returned list, choose Bot Channels Registration  
6. Click create in the blade that opens
7. Provide a Name for your bot
8. Choose the same Subscription where you deployed your bot’s code
9. Pick your existing Resource group which will set the location
10. You can choose the F0 Pricing tier for development and testing
11. Enter your bot’s URL. Make sure you start with HTTPS and that you add the /api/messages, i.e. *https://yourbotname.azurewebsites.net/api/messages*
12. Turn off Application Insights for now
13. Click the Microsoft App ID and password
14. In the new blade click Create New

Note: you can use an auto-created App ID and Password, but the deployment will not display them to you, and you WILL have to go into the azure deployment metadata to find it. If you chose this, skip to step 21.

15. In the new blade that opens to the right, click the "Create App ID in the App Registration Portal" which will open in a new browser tab  
16. In the new tab, click 'New Registration'. Fill in name and chose supported account types. Skip Redirect URI. Click 'Register'.
17. Copy and save your Application (client) ID
18. Click 'Certificates & Secrets'
19. Click 'new client secret'. Type 'Bot App Password' in description and select 'Never' for Expiration. Select 'Create'.
19. Copy and save the value of the Bot App Password somewhere you can get to later
20. Just close the browser tab and return to the Azure Portal tab
21. Paste in your App ID and Password in the correct fields and click OK
22. Now click Create to set up your channel registration. This can take a few seconds to a few minutes.

### **Update your bot’s Application Settings**

In order for your bot to authenticate with the Azure Bot Service, you need to add two settings to your Bot’s Application Settings in Azure App Service.

1. Click App Services. Type your bot’s name in the Subscriptions text box. Then click on your bot's name in the list.
2. Scroll until you find the Application settings section
3. Click 'New Application Setting'
4. Type MicrosoftAppId for the name and your App ID for the value
6. Click Add new setting
7. Type MicrosoftAppPassword for the name and your password for the value
8. Click the Save button up top

### **Test Your Bot in Production**

At this point, you can test your bot from Azure using the built-in Web Chat client:

1. Go back to your Resource group in the Azure portal
2. Open your bot
3. Under Bot management, select Test in Web Chat

## **Recommended Documents**

* [Deploy your bot](https://docs.microsoft.com/azure/bot-service/bot-builder-deploy-az-cli?view=azure-bot-service-4.0&tabs=csharp)
