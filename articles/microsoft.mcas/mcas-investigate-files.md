<properties
  pageTitle="I need help investigating files"
  description="I need help investigating files"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-investigate-files"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728982"
  resourceTags=""
  productPesIds="16031"
 ownershipId="CloudAppSecurity_DataProtection"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I need help investigating files

Most users are able to file investigation questions using the information below.

## **Recommended Steps**

1. If you cannot see Amazon Web Services (AWS) files. This is expected behavior as only AWS bucket level permissions are supported and hence Cloud App Security doesn't have visibility into the files contained in the buckets.
1. If you cannot see Office 365 files, including SharePoint Online and OneDrive, in Cloud App Security, in the Office 365 connector settings, verify that you have enabled "Office 365 files".
1. If you are unable to export more than 5000 results in the Microsoft Cloud App Security portal. This is expected behavior as the portal is limited to 5000 results. If you need to export more results, use the [Cloud App Security REST API](https://docs.microsoft.com/cloud-app-security/api-alerts-list).

## **Recommended Documents**

- [Investigate files](https://docs.microsoft.com/cloud-app-security/file-filters)
- [Connected apps](https://docs.microsoft.com/cloud-app-security/enable-instant-visibility-protection-and-governance-actions-for-your-apps)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
