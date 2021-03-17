<properties
	pageTitle="Find out what kind of HTTP 502 error you are seeing"
	description="Find out what kind of HTTP 502 error you are seeing"
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
	articleId="7166cd72-e5db-4d9e-ab8d-7ed2db2c1b4c"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Find out what kind of HTTP 502 error you are seeing

1. HTTP 502 is a general error message for all problems when communicating with the customer's Bot. All non-200 statuses returned by the customer's bot code are translated into 502 at the client end. To find the internal error you can use ASC or Applens
2. To use ASC, go to [ASC](https://azuresupportcenter.msftcloudes.com) and enter the case number. On the overview page look for any HTTP error insights that may have been generated. You can also force to run insights by selecting edit and run option at the top right corner.
3. To use Applens, go to [ASC](https://azuresupportcenter.msftcloudes.com) and enter the case number and go to 'Resource Explorer' and click on Applens link. Once you are on the Applens page, on the left hand pane, click on Availability and Performance under Detectors.
4. Explore 'Result codes returned from posts to bot endpoint' and 'Bot Basic Details' for finding relevant HTTP errors

