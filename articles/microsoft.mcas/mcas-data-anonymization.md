<properties
  pageTitle="I'm having issues with data anonymization in Discovery"
  description="I'm having issues with data anonymization in Discovery"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-data-anonymization"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728971"
  resourceTags=""
  productPesIds="16031"
 ownershipId="CloudAppSecurity_Discovery"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues with data anonymization in Discovery

Most users are able to resolve data anonymization questions using the information below.

## **Recommended Steps**

**Which data sources can be anonymized?**

Cloud App Security only anonymizes new data from data sources created, or updated, after enabling the anonymization feature.

For data sources that exist prior to enabling data anonymization, use the following steps to enable anonymization:

1. For log collectors, [delete all discovery data](https://docs.microsoft.com/cloud-app-security/discovered-apps#deleting-cloud-discovery-data), and then for each log collector whose data you want to anonymize, [enable anonymization](https://docs.microsoft.com/cloud-app-security/cloud-discovery-anonymizer#how-data-anonymization-works) for the collector

1. For Microsoft Defender Advanced Threat Protection (ATP), disable the integration and then enable it again

**NOTE**  
It's important to be sure you want to delete data before continuing - it can't be undone and it deletes **all** Cloud Discovery data in the system.

**What types of data can be anonymized?**

You can apply data anonymization for usernames, and for Windows 10 endpoint users you can additionally anonymize machine names.

1. Under the Settings cog, select **Cloud Discovery settings**
1. In the Anonymization tab, to anonymize usernames by default, select **Anonymize private information by default in new reports and data sources**. You can also select **Anonymize machine information by default in 'Win10 Endpoint Users' report**
1. Click **Save**

**NOTE**: IP addresses and subdomains are not anonymized.

**How do I deanonymize multiple users?**

- To deanonymize usernames in bulk, use the steps in [Cloud Discovery data anonymization](https://docs.microsoft.com/cloud-app-security/cloud-discovery-anonymizer), under **To resolve multiple usernames**

## **Recommended Documents**

- [Cloud Discovery data anonymization](https://docs.microsoft.com/cloud-app-security/cloud-discovery-anonymizer)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
