<properties
  pageTitle="I'm having issues with receiving email notifications"
  description="I'm having issues with receiving email notifications"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-portal-email-notifications"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728975"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_Portal"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues with receiving email notifications

Most users are able to resolve email notification issues using the steps below.

## **Recommended Steps**

1. If you are not receiving admin email notifications, verify that your [admin settings](https://docs.microsoft.com/cloud-app-security/admin-settings) are configured correctly.
1. If your users are not receiving email notifications, do the following:
    1. Verify that [email notifications for end-users](https://docs.microsoft.com/cloud-app-security/mail-settings) are properly configured.
    1. For governance action notifications, verify the intended recipient is configured correctly. For example, for [file owner notification actions](https://docs.microsoft.com/cloud-app-security/governance-actions#governance-log), verify that the intended recipient is the owner of the file.
1. Verify that you have configured the [network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements#mail-server) for your mail server.
1. Check the recipient's spam folder for the missing email notifications.
1. Check the [current status](https://status.cloudappsecurity.com/) of Microsoft Cloud App Security to see if there was a scheduled maintenance or known issue in the service you are using, at the time of the event.

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
