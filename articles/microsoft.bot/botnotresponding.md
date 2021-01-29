<properties
  pagetitle="My bot is not responding or times out"
  service="microsoft.botservice"
  resource="botservices"
  ms.author="jameslew"
  selfhelptype="Resource"
  supporttopicids="32688621"
  resourcetags=""
  productpesids="16152"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="d0e4ed4e-30f4-4c0c-acc5-3f615f1f4f70"
  ownershipid="Compute_BotService" />
# My bot is not responding or times out

When a user sends a message to a bot, the bot must send an HTTP acknowledgment that it received the request. If the bot fails to acknowledge within 15 seconds, an error is logged within the channel where the user sent the request.

The Direct Line and Web Chat channels transmit these errors back to client software with HTTP 502 and 504 errors. Other clients, such as Teams and Cortana, do not present a programmatic code to the user.

The cause of this failure is typically within the bot's source code, a configuration error (such as an incorrect endpoint), or a transient problem such as a networking failure.

**Note**: A bot can successfully acknowledge the HTTP request without sending a reply. If the bot is accepting requests but is not responding, that problem must be debugged within the bot's conversational logic.

## **Recommended Steps**

1. Use the [bottroubleshooter community tool](https://github.com/BotBuilderCommunity/botbuilder-community-tools/tree/master/bottroubleshooter) to analyze the bot's configuration and look for obvious errors
2. Verify that your client supports [TLS 1.2](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2-client) encryption
3. Use the [Bot Framework emulator](https://github.com/Microsoft/BotFramework-Emulator/releases) to connect directly to the bot's cloud endpoint to see if it functions properly
4. If the problem only occurs when the bot is first starting, and the bot is hosted on an Azure Web App, consider enabling the AlwaysOn option (Note: this might increase the cost of running the bot)
5. Enable Application Insights and connect it to both the bot's source code and its Bot Service registration in Azure to log any exceptions that may be occurring within the bot: [ASP.NET](https://docs.microsoft.com/azure/azure-monitor/app/asp-net), [ASP.NET Core](https://docs.microsoft.com/azure/azure-monitor/app/asp-net-core)
6. To view Application Insights logs, navigate to AppInsights blade, then click "All App service settings", then "Application Insights" button and then "View Application Insights data", then "Analytics" button
7. Query for timeout exceptions. The following query will tell you the most recent exceptions in your bot: 

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