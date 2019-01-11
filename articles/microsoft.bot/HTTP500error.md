<properties
	pageTitle="I'm seeing HTTP 500 exceptions reported by my bot"
	description="I'm seeing HTTP 500 exceptions reported by my bot"
	service="microsoft.bot"
	resource="botservice"
	authors="arturl,meetshamir"
	authorAlias="arturl,saziz"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16152,16442,16673"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
/>

# I'm seeing HTTP 500 exceptions reported by my bot

## **Recommended steps**
	1. Enable Application Insights (ASP.NET, ASP.NET Core). 

	1. Navigate to AppInsights blade. Click "All App service settings", then "Application Insights" button and then "View Application Insights data", then "Analytics" button.
	
	1. Query for exceptions. The following query will tell you the most recent exceptions in your bot:
	exceptions 
  | order by timestamp desc
  | project timestamp, operation_Id, appName 
	
	1. From this query, select a few operation_Id's and then look for more information:
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
	
	1. If you have only exceptions, analyze the details and see if they correspond to anywhere in your code. If you only see exceptions coming from the Channel Connector (Microsoft.Bot.ChannelConnector) then ensure that Application Insights is set up correctly and your code is logging events.


## **Recommended documents**
Troubleshooting  Bot Timeout Errors
Troubleshooting Application Insights setting for ASP.NET Web App
Troubleshooting Application Insights setting for ASP.NET Core Web App
