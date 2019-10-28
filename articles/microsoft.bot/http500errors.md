<properties
	pageTitle="I'm seeing HTTP 500 exceptions reported by my bot"
	description="I'm seeing HTTP 500 exceptions reported by my bot"
	service="Microsoft.BotService"
	resource="botServices"
	authors="arturl,meetshamir"
	ms.author="arturl,saziz"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32688623, 32688619"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="ce6a5a39-cbfa-4212-a68c-a282adfbac0e"
/>

# I'm seeing HTTP 500 exceptions reported by my bot

## **Recommended Steps**

1. Enable Application Insights (ASP.NET, ASP.NET Core)
2. Navigate to AppInsights blade and click "All App service settings", then "Application Insights" 
3. Navigate to "View Application Insights data" and click the "Analytics" button
4. Query for exceptions. The following query will tell you the most recent exceptions in your bot:

```
	exceptions
	| order by timestamp desc
	| project timestamp, operation_Id, appName
```

5. From this query, select a few operation_Ids and look for more information:

```
	let my_operation_id = "d298f1385197fd438b520e617d58f4fb";
	let union_all = () {
		union
		(traces | where operation_Id == my_operation_id),
		(customEvents | where operation_Id == my_operation_id),
		(requests | where operation_Id == my_operation_id),
		(dependencies | where operation_Id  == my_operation_id),
		(exceptions | where operation_Id == my_operation_id)
	};
	union_all
	| order by timestamp desc
```

6. If you have only exceptions, analyze the details and see if they correspond to anywhere in your code. If you only see exceptions coming from the Channel Connector (Microsoft.Bot.ChannelConnector) then ensure that Application Insights is set up correctly and your code is logging events.
	
## **Recommended Documents**

* [Troubleshooting  Bot Timeout Errors](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-500-errors?view=azure-bot-service-4.0&tabs=dotnetwebapi) <br>
* [Troubleshooting Application Insights setting for ASP.NET Web App](https://docs.microsoft.com/azure/azure-monitor/app/asp-net)<br>
* [Troubleshooting Application Insights setting for ASP.NET Core Web App](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core)<br>
