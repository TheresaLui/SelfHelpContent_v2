<properties
	pageTitle="I am not receiving my notifications"
	description="General trouble-shooting guide for Action Group notifications"
	infoBubbleText="Some suggestions have been found to help solve your alert / action group notification issue more quickly."
	service="microsoft.insights"
	resource="actiongroups"
	authors="dkamstra, snehithm"
	ms.author="dukek, snmuvva"
	displayOrder="5"
	articleId="insights-missingnotifications"
	selfHelpType="generic"
	supportTopicIds="32629650,32629653,32629654,32629655,32629656,32629658"
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake"
/>

# I am not receiving notifications even though my alert triggered

Most alerts in Azure Monitor use [Action Groups](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-action-groups) as the notification delivery mechanism. If you are sure the alert was triggered but you are not receiving notifications, following the recommended steps will help you resolve this issue.

## **Recommended Steps**

### Email

* Ensure your email system and your inbox are configured to accept email from these email addresses: azure-noreply@microsoft.com, azureemail-noreply@microsoft.com, and alerts-noreply@mail.windowsazure.com
* Email is rate limited to no more than 100 emails every hour to each email address. Check your email inbox for a message indicating that your email address has been rate limited. If you need to avoid rate limiting, we suggest you use the Webhook, LogicApp, or Runbook actions (none of which are rate limited).
* Check if you have any inbox rules set to divert emails from the send from addresses to a Junk folder or any other folder
* Check if you have unsubscribed from email notifications by searching for an Unsubscribe confirmation email in your inbox. You may resubscribe to email notifications by using the link in the Unsubscribe email, or by removing then recreating the Email action in your action group

### SMS and Voice

* Verify that your phone number is correct
* Verify that you have not blocked the phone number or short code that Azure uses to send the SMS or make the phone call
* Verify that your wireless carrier has not blocked the phone number or short code
* SMS and Voice are rate limited to no more than 1 notification every 5 minutes for each target phone number. Check your SMS for a message indicating that your phone number has been rate limited. If you need to avoid rate limiting we suggest you use the Webhook, LogicApp, or Runbook actions (none of which are rate limited).
* Check your SMS thread history to see if you have opted out of SMS delivery from the action group using the DISABLE or STOP command. You can resubscribe to notifications by removing, then recreating, the SMS action in your action group.

### Webhook

* Whitelist the [IP addresses](https://go.microsoft.com/fwlink/?linkid=827201#action-specific-information) the webhook will be called from:

	* 13.106.57.181
	* 13.106.54.3
	* 13.106.54.19
	* 13.106.38.142
	* 13.106.38.148
	* 13.106.57.196

* Verify the webhook endpoint you have configured is correct and the endpoint is working correctly
* If you are using webhooks to [integrate with Teams or Slack](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups-logic-app), the endpoint expects the payload in a certain format which is different from what alerts provide
* The timeout period for a response is 10 seconds. The webhook call will be retried a maximum of 2 times when the following HTTP status codes are returned: 408, 429, 503, 504, or the HTTP endpoint does not respond. The first retry happens after 10 seconds. The second and last retry happens after 100 seconds. If the second retry fails the endpoint will not be called again for 30 minutes for any action group.

## **Recommended Documents**

* [Email, webhook and other action specific information](https://go.microsoft.com/fwlink/?linkid=827201#action-specific-information)<br>
* [Creating and managing action groups](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-action-groups)<br>
* [Pricing information for action group notifications](https://azure.microsoft.com/pricing/details/monitor/)
