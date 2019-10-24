<properties
	pageTitle="My bot is not responding or times out"
	description="My bot is not responding or times out"
	service="Microsoft.BotService"
	resource="botServices"
	authors="arturl,meetshamir"
	ms.author="arturl,saziz"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32688621"
	resourceTags=""
	productPesIds="16152"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	articleId="d0e4ed4e-30f4-4c0c-acc5-3f615f1f4f70"
/>

# My bot is not responding or times out

Timeout errors usually manifest themselves as HTTP GatewayTimeout errors (504). This happens when the bot fails to respond to the Bot Framework within 15 seconds. 

[The bottroubleshooter community tool](https://github.com/BotBuilderCommunity/botbuilder-community-tools/tree/master/bottroubleshooter) can help identify certain issues. Please download the troubleshooter and follow the guidance as detailed in there.

## **Recommended Steps**

1. Analyze your bot behavior and make sure it doesn’t make external calls (to storage or other services) that take longer than 15 seconds
2. If the bot is receiving large volume of traffic, consider scaling it out and changing it to use Web Sockets (for bots using Direct Line)
3. If the bot doesn't have AlwaysOn option set, consider setting it (Note: it might increase the cost of running the bot)
4. Enable Application Insights ([ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net), [ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core))
5. Navigate to AppInsights blade, then click "All App service settings", then "Application Insights" button and then "View Application Insights data", then "Analytics" button
6. Query for timeout exceptions. The following query will tell you the most recent exceptions in your bot: 

```
	exceptions 
	| order by timestamp desc
	| where type == "Microsoft.Bot.Schema.BotTimeoutException" 
	| project timestamp, operation_Id, appName 
```

7. From this query, select a few operation_Ids and look for more information:

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

8. If you have only exceptions, analyze the details and see if they correspond to anywhere in your code. If you only see exceptions coming from the Channel Connector (Microsoft.Bot.ChannelConnector) then ensure that Application Insights is set up correctly and your code is logging events.

## **Recommended Documents**

* [Troubleshoot HTTP 500 errors](https://docs.microsoft.com/azure/bot-service/bot-service-troubleshoot-500-errors?view=azure-bot-service-4.0&tabs=dotnetwebapi)


