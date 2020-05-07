<properties
    pageTitle="Did not receive expected email"
    description="I can see my fired alert in the Azure portal, but did not receive its email"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="alerts"
    authors="ofirmanor"
    ms.author="ofmanor"
    displayOrder="1"
    articleId="alerts-notification-missing-email"
    selfHelpType="generic"
    supportTopicIds="32739779"
    productPesIds="15454,15725"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# I didn't receive an email as expected 

## **Recommended Steps**

If you can see a fired alert in the Azure portal, but did not receive the email that you have configured about it, follow these steps:

**1. Was the email suppressed by an [action rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules)?**

Check by clicking on the fired alert in the portal, and look at the history tab for suppressed [action groups](https://docs.microsoft.com/azure/azure-monitor/platform/action-groups):

![alert details history tab with action group suppression](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/history-action-rule.png)

If that was unintentional, you can modify, disable, or delete the action rule.

**2. Is the type of action "Email Azure Resource Manager Role"?**

This action only looks at Azure Resource Manager (ARM) role assignments that are at the subscription scope, and of type User. Make sure that you have assigned the role at the subscription level, and not at the resource level or resource group level.

**3. Are your email server and mailbox accepting external emails?**

Verify that emails from these three addresses are not blocked:

* azure-noreply@microsoft.com
* azureemail-noreply@microsoft.com
* alerts-noreply@mail.windowsazure.com

It is common that internal mailing lists or distribution lists block emails from external email addresses. You need to whitelist the above email addresses.

To test, add a regular work email address (not a mailing list) to the action group and see if alerts arrive to that email.

**4. Was the email processed by inbox rules or a spam filter?**

Verify that there are no inbox rules that delete those emails or move them to a side folder. For example, inbox rules  could catch specific senders or specific words in the subject.

Also, check:

* the spam settings of your email client (like Outlook, Gmail)
* the sender limits / spam settings / quarantine settings of your email server (like Exchange, Office 365, G-suite)
* the settings of your email security appliance, if any (like Barracuda, Cisco)

**5. Have you accidentally unsubscribed from the action group?**

The alert emails provide a link to unsubscribe from the action group. To check if you have accidentally unsubscribed from this action group, either:

* Open the action group in the portal and check the Status column:

    ![action group status column](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/action-group-status.png)
* Search your email for the unsubscribe confirmation:

    ![unsubscribed from alert action group](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/unsubscribe-action-group.png)

To subscribe again – either use the link in the unsubscribe confirmation email you have received, or remove the email address from the action group, and then add it back again.

**6. Have you been rated limited due to many emails going to a single email address?**

Email is [rate limited](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-rate-limiting) to no more than 100 emails every hour to each email address. If you pass this threshold, additional email notifications are dropped. Check if you have received a message indicating that your email address has been temporarily rate limited:

![Email rate limited](https://docs.microsoft.com/azure/azure-monitor/platform/media/alerts-troubleshoot/email-paused.png)

If you would like to receive high-volume of notifications without rate limiting, consider using a different action, such as webhook, logic app, Azure function, or automation runbooks, none of which are rate limited.
