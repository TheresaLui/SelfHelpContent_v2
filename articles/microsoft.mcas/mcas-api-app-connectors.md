<properties
  pageTitle="I'm having issues with connecting/disabling app connectors"
  description="I'm having issues with connecting/disabling app connectors"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-api-app-connectors"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728968"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_API"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues with connecting/disabling app connectors

Most users are able to app connector issues using the steps below.

## **Recommended Steps**

* If you are having a problem adding a connector, see the [relevant connector documentation](https://docs.microsoft.com/cloud-app-security/enable-instant-visibility-protection-and-governance-actions-for-your-apps)
* If you are getting the errors "connection error" or "no recent status":
    
  * Go to the relevant app and perform a **Test now** check
  * If you are still getting an error, try to resolve the issue using the [troubleshooting guide](https://docs.microsoft.com/cloud-app-security/troubleshooting-api-connectors-using-error-messages)
  
* If the connector is working by you can't see users or activities from the connector, use the following guidelines:
    
  * Allow up to 72 hours for the first scan to complete
  * After this period, if you there are still missing activities, proceed to open the support case and make sure you provide examples of activities from the service's audit log that are not appearing in Cloud App Security with the ticket
  
* If you want to disable a connector, see [disabling a connector](https://docs.microsoft.com/cloud-app-security/enable-instant-visibility-protection-and-governance-actions-for-your-apps#disable-app-connectors)

**Note**: You can disable connectors but you can't remove them.

* If you want to re-enable a connector, see [re-enable a connector](https://docs.microsoft.com/cloud-app-security/enable-instant-visibility-protection-and-governance-actions-for-your-apps#re-enable-app-connectors)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
