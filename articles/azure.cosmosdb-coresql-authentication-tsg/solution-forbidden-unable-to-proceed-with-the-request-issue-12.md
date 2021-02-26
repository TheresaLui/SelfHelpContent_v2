<properties
	  pageTitle="Forbidden Unable to proceed with the request issue"
	  description="Forbidden Unable to proceed with the request issue"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="835bdeff-7d30-433a-835f-5526ebf51161"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Forbidden Unable to proceed with the request issue

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** 
1. If you customer gets an error message like so:

*Unable to proceed with the request. Please check the authorization claims to ensure the required permissions to process the request.*

This is likely due to firewall, get the ActivityId for the request and look in FrontendEvent table:

2. We can use a Kusto query like this
```
FrontendEvent
| where TIMESTAMP > datetime(2019-03-22 15:20:49.5158252) - 24h and TIMESTAMP < datetime(2019-03-22 15:20:49.5158252) + 12h
| where ActivityId == "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
```
(Remove the TIMESTAMP filter if you're not sure when it happened, but it will take longer)

3. if you see an error message saying that the IP Address is not whitelisted, then that is the cause of the error:

- EventName="FormattedMessageEvent" FormattedMessage="Global databaseAccount {0}, use regional DatabaseAccountRequestProcessor {1}" Argument0="**xxxxxxxx**" Argument1="xxxxxxxx-southcentralus" TraceSource="DocDBTrace"
- EventName="FormattedMessageEvent" FormattedMessage="**Client IPAddress: {0} not whitelisted, request will be blocked" Argument0="xxx.xxx.xx.x" TraceSource="DocDBTrace**"
- EventName="FormattedMessageEvent" FormattedMessage="Request is blocked by firewall in Gateway. IP info: IP Address = xxx.xxx.xx.x, It is blocked by VNET filter. databaseAccountId = **xxxxxxxx**-southcentralus, ipFilterEnabled = True, ipFilter = xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x/32,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x/32,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x,xxx.xxx.xx.x, vnetFilterEnabled = True, vnetFilter = xxxxxxxx:3,xxxxxxxx:2,xxxxxxxx:1" TraceSource="DocDBTrace"
- EventName="FormattedMessageEvent" FormattedMessage="DocumentClientException with status code {0}, message: {1}, inner exception: {2}, and response headers: {3}" Argument0="Forbidden" Argument1="Unable to proceed with the request. Please check the authorization claims to ensure the required permissions to process the request." Argument2="null" Argument3="null" TraceSource="DocDBTrace"
 

4. Be sure to double check the **global database account name** matches what the customer expects.


#### KUSTO:

5. You can verify their current settings in the MgmtGlobalDatabaseAccountTrace table:
```
MgmtGlobalDatabaseAccountTrace
| where TIMESTAMP > datetime(2019-03-22 15:20:49.5158252) - 24h 
    and TIMESTAMP < datetime(2019-03-22 15:20:49.5158252) + 12h
| where GlobalDatabaseAccount == "xxxxxxxx"
```

6. Look in the IPRangeFilter column and you can confirm that. Look at their latest settings to see if they've changed it (sometimes customer will remove the IP filter after the error, but still demand an RCA, so you need to look historically around the time of the issue)

7. If this isn't the cause, engage the Ops queue and they'll triage if it is an SDK issue or a backend issue. You 100% need an activity id before you engage the product group. They cannot help without it. Include the above queries in it.


## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query to customer.


<!--/issueDescription-->

