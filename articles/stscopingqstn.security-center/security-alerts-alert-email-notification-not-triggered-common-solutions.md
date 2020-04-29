<properties
    pageTitle="Security Alerts - Alert email notification not triggered Common Solutions"
    description="Security Alerts - Alert email notification not triggered Common Solutions"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636859"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="c3eaf0dd-97cf-4d12-83f6-f39126a72887"
	ownershipId="Azure_Security_Security_Center"
/>

# Security Alerts - Alert email notification not triggered Common Solutions

An email notification is sent on the first daily occurrence of an alert, and only for high severity alerts. Email preferences can be configured only for subscription policies. Resource groups within a subscription will inherit these settings.

Alert email notifications are sent per the following guidelines:

* Only for high severity alerts<br>
* To a single email recipient per alert type, per day

No more than three (3) email messages are sent to a single recipient in a single day, and each email message contains a single alert, not an aggregation of alerts.

If customers want to send emails on alerts that have a severity lower than **High**, they can configure the alert based on [this blog post](https://blogs.technet.microsoft.com/yuridiogenes/2018/08/01/using-azure-monitor-to-send-an-email-notification-for-azure-security-center-alerts/)

If customers want to check their alert notification, they should follow the alert validation process. **Alerts Validation** in **Azure Security Center** will then raise an alert, and send an email to the user or distribution list configured in the email preferences in **Azure Security Center**.

## **Recommended Documents**

* [Managing and responding to security alerts in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-managing-and-responding-alerts)<br>
* [Understanding security alerts in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-alerts-type)<br>
* [Tutorial: Respond to security incidents](https://docs.microsoft.com/azure/security-center/tutorial-security-incident)<br>
* [Alerts Validation in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-alert-validation)<br>
* [Email Notifications in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-provide-security-contact-details)<br>
* [Handling Security Incidents in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-incident)<br>
* [Alert confidence score](https://docs.microsoft.com/azure/security-center/security-center-confidence-score)<br>
* [Investigate Incidents and Alerts in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-investigation)<br>
* [Azure Security Center detection capabilities](https://docs.microsoft.com/azure/security-center/security-center-detection-capabilities)

## Troubleshooting

* [ASC Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

## FAQ

* [ASC FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)