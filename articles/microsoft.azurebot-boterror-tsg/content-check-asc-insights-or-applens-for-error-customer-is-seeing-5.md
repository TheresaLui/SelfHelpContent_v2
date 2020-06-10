<properties
	pageTitle="Check ASC Insights or Applens for error customer is seeing"
	description="Check ASC Insights or Applens for error customer is seeing"
	service="Microsoft.BotService"
	resource="Microsoft.BotService/botServices"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="408e695d-57b5-4ba1-bc59-56bab34d13d5"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check ASC Insights or Applens for error customer is seeing

1. Ask the customer the error code they are seeing in the code or from the service
2. You can use ASC or Applens to identify an error
3. To use ASC, go to [ASC](https://azuresupportcenter.msftcloudes.com) and enter the case number. On the overview page look for any HTTP error insights that may have been generated. You can also force to run insights by selecting edit and run option at the top right corner.
4. To use Applens, go to [Applens](https://applens.azurewebsites.net) and under 'Resource Type' select ARM Reource ID and enter the resource details in the below format:
 /subscriptions/<subscription ID>/resourceGroups/<Resource Group name>/Microsoft.BotService/botServices/<Bot name> 
5. Replace the subscription ID, Resource Group name and the Bot name
    1. Example: /subscriptions/c65a65de-d22c-4c2a-9ff4-aefcca7753a7/resourceGroups/Shamir-WebAppBot/providers/Microsoft.BotService/botServices/saziz-testbot 
6. Select appropriate time period and hit go. 
7. On the left hand pane, click on Availability and Performance under Detectors. Explore
    1. 'Result codes returned from posts to bot endpoint' and 'Bot Basic Details' for finding relevant HTTP errors. 
    2. 'Bot P95 Latency (in ms)' to see if the Bot is slow to respond
    3. 'Connector Incoming Request Latency' 

