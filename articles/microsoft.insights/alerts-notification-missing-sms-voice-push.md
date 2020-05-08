<properties
    pageTitle="Did not receive expected SMS, voice call, or push notification"
    description="I can see my fired alert in the Azure portal, but did not receive its SMS, push notification, or voice call"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="alerts"
    authors="ofirmanor"
    ms.author="ofmanor"
    displayOrder="2"
    articleId="alerts-notification-missing-sms-voice-push"
    selfHelpType="generic"
    supportTopicIds="32739781"
    productPesIds="15454,15725"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# I didn't receive an expected SMS, voice call, or push notification

## **Recommended Steps**

If you can see a fired alert in the portal, but did not receive the SMS, voice call or push notification that you have configured about it, follow these steps:

**1. Was the action suppressed by an [action rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules)?**

Check by clicking on the fired alert in the portal, and look at the history tab for suppressed [action groups](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups):

![alert details history tab with action group suppression](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/history-action-rule.png)

If that was unintentional, you can modify, disable, or delete the action rule.

**2. SMS / voice: Is your phone number correct?**

Check the SMS action for typos in the country code or phone number.

**3. SMS / voice: have you been rate limited?**

SMS and voice calls are [rate limited](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-rate-limiting) to no more than one notification every five minutes per phone number. If you pass this threshold, the notifications will be dropped.

* Voice call – check your call history and see if you had a different call from Azure in the preceding five minutes.
* SMS - check your SMS history for a message indicating that your phone number has been rate limited.

If you would like to receive high-volume of notifications without rate limiting, consider using a different action, such as webhook, logic app, Azure function, or automation runbooks, none of which are rate limited.

**4. SMS: Have you accidentally unsubscribed from the action group?**

Open your SMS history and check if you have opted out of SMS delivery from this specific action group (using the DISABLE _action_group_short_name_ reply) or from all action groups (using the STOP reply). To subscribe again, either send the relevant SMS command (ENABLE _action_group_short_name_ or START), or remove the SMS action from the action group, and then add it back again.

For more information, see [SMS alert behavior in action groups](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-sms-behavior).

**5. Have you accidentally blocked the notifications on your phone?**

Most mobile phones allow you to block calls or SMS from specific phone numbers or short codes, or to block push notifications from specific apps (such as the Azure mobile app). To check if you accidentally blocked the notifications on your phone, search the documentation specific for your phone operating system and model, or test with a different phone and phone number.
