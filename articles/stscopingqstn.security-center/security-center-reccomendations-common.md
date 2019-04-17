<properties
    pageTitle="Azure Security Center Data and Storage Recommendation Common Solutions"
    description="Azure Security Center Data and Storage Recommendation Common Solutions"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32633032,32633085"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public"
    articleId="a15f057d-9001-4b77-a98a-dfaf3843dc2f"
/>

# Azure Security Center Data and Storage Recommendation Common Solutions

Azure Security Center analyzes the security state of your Azure resources. When Azure Security Center identifies potential security vulnerabilities, it creates recommendations that guide you through the process of configuring the needed controls. Azure Security Center monitors the following resources: virtual machines (VMs), networking, SQL and data, and applications. You can [disable recommendations from Azure policy](https://docs.microsoft.com/en-us/azure/security-center/security-center-faq#how-do-i-disable-data-collection).

## **Top issues**

**A given recommendation disappears from Security Center**

The given recommendation will disappear if one of the following conditions is true:

- All the resources under this recommendation become healthy.
- The recommendation is disable from the Azure policy.

**How often do the recommendations get refreshed?**

The recommendations are refreshed every 12 hours.

**Can I turn off the email alerts via email or customize the recipient list?**

No. These are currently not supported. Alert emails are sent to the subscription admin, there is no way to customize it. However this feature is coming soon.

**I received the alerts, but how do I investigate it?**

There is a lot of information that can be used for investigation in the alert email. We recommend you to use [diagnostics logs](https://docs.microsoft.com/en-us/azure/storage/common/storage-monitor-storage-account#configure-logging) for better investigation capabilities.

**Limitations**

- Advanced Threat Protection for Azure Storage is currently available only for the Blob storage
- Advanced Threat Protection for Azure Storage is not available in sovereign clouds.
- Advanced Threat Protection for Azure Storage is not available in France regions.

## **Recommended Documents**

- [Azure Storage Advanced Threat Protection](https://docs.microsoft.com/azure/storage/common/storage-advanced-threat-protection)
- [Protecting Azure SQL service and data in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-sql-service-recommendations)
- [Azure Security Center Data Security](https://docs.microsoft.com/azure/security-center/security-center-data-security)
- [Data collection in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection)
- [Manage user data in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-investigation-user-data)

**Storage Recommendations**

- [Enable Encryption For Storage Account](https://docs.microsoft.com/azure/security-center/security-center-enable-encryption-for-storage-account)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/en-us/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
- [Pricing details](https://azure.microsoft.com/pricing/details/security-center/).
