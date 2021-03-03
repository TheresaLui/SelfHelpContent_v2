<properties
  pageTitle="I'm having issues around External SIEM Solution"
  description="I'm having issues around External SIEM Solution"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-api-external-siem"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728977"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_API"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues around External SIEM Solution

Most users are able to resolve external SIEM solutions integration issues using the following steps.

## **Recommended Steps**

1. If you need help with setup and architecture design, see [Generic SIEM integration](https://docs.microsoft.com/cloud-app-security/siem)

    **Note:** After the initial setup of the SIEM agent with Cloud App Security, activities and alerts will be forwarded to the SIEM based on the filter you selected when configuring the SIEM. The SIEM will receive information for the preceding two days and onwards.

1. If the SIEM disconnects periodically, make sure that the [JAR file](https://docs.microsoft.com/cloud-app-security/siem#step-2-download-the-jar-file-and-run-it-on-your-server) is running on startup on your server
1. If encounter delays in receiving events, check the Cloud App Security [status page](https://status.cloudappsecurity.com/) for any known issues that could affect your environment
1. If you are missing events, check the [SIEM agent log](https://docs.microsoft.com/cloud-app-security/siem#step-2-download-the-jar-file-and-run-it-on-your-server) and look for any network errors. If there are no errors, follow the [recover missing activity events in SIEM Agent](https://docs.microsoft.com/cloud-app-security/troubleshooting-siem#recover-missing-activity-events-in-cloud-app-security-siem-agent) to try to identify the problem.

If you're still experiencing the issue after reviewing the documentation and configuration, continue with opening the ticket.
