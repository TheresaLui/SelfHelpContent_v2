<properties
    pageTitle="Email notifications Common Solutions"
    description="Email notifications Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680781"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a25f057d-8ce6-4b77-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Email Notifications Common Solutions

Azure Security Center will recommend that you provide security contact details for your Azure subscription. An email notification is sent on the first daily occurrence of an alert and only for high severity alerts. Email preferences can only be configured for subscription policies. Resource groups within a subscription will inherit these settings.

**Tips for Email Notifications**

Alert email notifications are sent:

- Only for high severity alerts
- To a single email recipient per alert type per day
- No more than three email messages are sent to a single recipient in a single day
- Each email message contains a single alert, not an aggregation of alerts

For example, if an email message was already sent to alert you about an RDP attack, you will not receive another email message about an RDP attack on the same day, even if another alert is triggered.

## **Recommended Documents**

- [Azure Security Center Email Notifications](https://docs.microsoft.com/azure/security-center/security-center-provide-security-contact-details)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
