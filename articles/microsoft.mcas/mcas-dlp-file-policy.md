<properties
  pageTitle="I'm having a problem with DLP and file policies"
  description="I'm having a problem with DLP and file policies"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-dlp-file-policy"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728974"
  resourceTags=""
  productPesIds="16031"
 ownershipId="CloudAppSecurity_DataProtection"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having a problem with DLP and file policies

Most users are able to resolve DLP and file policy questions using the information below.

## **Recommended Steps**

1. If you are sharing files and the domain isn't detected. This can occur when sharing files with external users using a group and the "Collaborators" filter is set to "Any from domain". In this setup, domains are not detected for members of a group and can only be detected for users who have direct permissions on the file.
1. If your data classification service sensitive types aren't matching as expected. Review the conditions of each [sensitivity type](https://docs.microsoft.com/microsoft-365/compliance/sensitive-information-type-entity-definitions) and, in the advanced settings, verify that each sensitive type' match accuracy and instance counts are configured correctly.
1. If you are unable to investigate and control files, verify that file monitoring is enabled. In Cloud App Security, select **Settings** > **Files**, and then click **Enable file monitoring**.  
**Note:** If you don't access the **Files** page for more than 60 days and have no active file policies, file monitoring will be automatically disabled.

## **Recommended Documents**

- [Session policies](https://docs.microsoft.com/cloud-app-security/session-policy-aad)
- [File policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies)
- [Sensitive information type entity definitions](https://docs.microsoft.com/microsoft-365/compliance/sensitive-information-type-entity-definitions)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
