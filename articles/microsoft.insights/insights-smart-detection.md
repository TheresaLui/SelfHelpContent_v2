<properties 
    pageTitle="I have questions about Smart Detection"
    description="General questions about Smart Detection."
    infoBubbleText="Some common questions and answers have been found to help address your Smart Detection questions."
    service="microsoft.insights"
    resource="components"
    authors="harelbr"
    ms.author="harelbr"
    articleId="insights-smart-detection"
    diagnosticScenario="SmartDetection"
    displayOrder="7"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32613001"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>

# I have questions about Smart Detection

**Why am I getting Smart Detection notifications?**<br>

[Smart Detection](https://docs.microsoft.com/azure/azure-monitor/app/proactive-diagnostics) automatically detects and notifies you about a variety of issues and abnormal patterns in your application. Smart Detection is enabled by
default, and doesn't require any special setup. Detected issues are displayed in the **Smart Detection** blade.
In addition, all Smart Detection rules, except for rules marked as **Preview**, are configured by default to send email notifications when detections are found.

**Why am I not getting Smart Detection notifications?**<br>

Smart Detection uses a variety of Machine Learning algorithms to learn the normal behavior of your application, and warns you only in cases where a significant anomaly is found. You should not expect to get a Smart Detection notification for every spike or dip in your telemetry, because there are a number of factors at play deciding whether such behaviors are indeed anomalous and how significant they are.

**Why didn't I get an email notification about an issue detected by Smart Detection?**<br>

There could be a number of reasons for not getting an email notification for a detection you see in the Smart Detection blade:

1. The detection was created by a Smart Detection rule marked as **Preview**. Such rules don't issue email notifications.
2. The detection rule was configured not to send emails. Check the email configuration of the specific rule, by going to the **Smart Detection Settings**.
3. You are not associated with the subscription's Monitoring Reader or Monitoring Contributor roles. These roles are configured to receive email notifications from Smart Detection by default.
4. There were additional issues detected that day, and an email notification was sent only for one of those issues. We do that to prevent spamming.

**What should I do if I received a detection?**<br>

A detection doesn't mean that your app definitely has a problem. It's simply a suggestion about something you might want to look at more closely. There's a lot of information provided with each detection that should help you understand what happened, assess the impact and get started with diagnosing the issue.

**Can I configure Smart Detection?**<br>

You can configure the following settings for a smart detection rule:

* If the rule is enabled (the default is **true**)
* If email notifications should be sent to users associated with the subscription's Monitoring Reader and Monitoring contributor roles when a detection is found (the default is **true**)
* Any additional email recipients who should get a notification when a detection is found:

    * Email configuration is not available for Smart Detection rules marked as **Preview**

[Configuring Smart Detection rules can be done from the portal or via ARM template](https://docs.microsoft.com/azure/azure-monitor/app/proactive-diagnostics#smart-detection-email-notifications). 

**What is the Failure Anomalies alert rule?**<br>

[Failure Anomalies](https://docs.microsoft.com/azure/azure-monitor/app/proactive-failure-diagnostics) is a Smart Detection rule that automatically notifies you in near real time if your web app experiences an abnormal rise in the rate of failed requests or failed dependency calls.

This Smart Detection rule is available as an alert rule, and is created together with your Application Insights resource.

You are not charged for this alert rule.

**What is the "Application Insights Smart Detection" Action Group?**<br>

The "Application Insights Smart Detection" Action Group is created automatically together with the [Failure Anomalies](https://docs.microsoft.com/azure/azure-monitor/app/proactive-failure-diagnostics) alert rule (part of Smart Detection), to support triggering actions when this alert rule fires.

This Action Group is created in the following situations:

1. When you create a new Application Insights resource
2. When existing Failure Anomalies alert rules are being [migrated](https://azure.microsoft.com/updates/classic-alerting-monitoring-retirement/) to the new alerting platform

You are not charged for email or webhook actions triggered by this Action Group.

## **Recommended Documents**

* [Smart Detection in Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/proactive-diagnostics)<br>
* [Failure Anomalies in Smart Detection](https://docs.microsoft.com/azure/azure-monitor/app/proactive-failure-diagnostics)<br>
* [Manage Smart Detection rules using Azure Resource Manager templates](https://docs.microsoft.com/azure/azure-monitor/app/proactive-arm-config)<br>
