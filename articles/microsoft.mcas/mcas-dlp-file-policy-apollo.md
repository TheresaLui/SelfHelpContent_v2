<properties
  pageTitle="MCAS - DLP and file policies"
  description="MCAS - DLP and file policies"
  ms.author="esagmon"
  resource=""
  resourceTags=""
  service="microsoft.mcas"
  displayOrder="0"
  articleId="24f82494-9c25-4373-b3d1-cebfbe18ce81"
  selfHelpType="Apollo"
  supportTopicIds="32728974"
  SapId="9f3fa90f-696f-1a7b-0b50-81317185ecfb"
  productPesIds="16031"
  cloudEnvironments="public"
  ownershipId="CloudAppSecurity_DataProtection"
/>

# Welcome to our new guided troubleshooting experience for DLP and file policies

This experience provides common solutions, important documents, and relevant how-to videos.

:::Section Recommended Solution:::

## **Recommended Steps**

1. If you are sharing files and the domain isn't detected. This can occur when sharing files with external users using a group and the "Collaborators" filter is set to "Any from domain". In this setup, domains are not detected for members of a group and can only be detected for users who have direct permissions on the file.
1. If your data classification service sensitive types aren't matching as expected. Review the conditions of each [sensitivity type](https://docs.microsoft.com/microsoft-365/compliance/sensitive-information-type-entity-definitions) and, in the advanced settings, verify that each sensitive type' match accuracy and instance counts are configured correctly.
1. If you are unable to investigate and control files, verify that file monitoring is enabled. In Cloud App Security, select **Settings** > **Files**, and then click **Enable file monitoring**

**Note:** If you don't access the **Files** page for more than 60 days and have no active file policies, file monitoring will be automatically disabled.

To view the article on labels, Sensitive Information Types and Microsoft Information Protection, see [labels, Sensitive Information Types and Microsoft Information Protection](https://techcommunity.microsoft.com/t5/core-infrastructure-and-security/a-journey-to-holistic-cloud-protection-with-the-microsoft-365/ba-p/1341515)

## Follow the instructions in the how-to videos below to resolve your issue

<videoGroup>
    <video>
        <src>https://www.youtube.com/watch?v=ZY1n7b29KtE&list=PLXPr7gfUMmKxS1SYNgDaQY-9Q6cOqFxvG&index=12</src>
        <title>How to label and protect all your data in the cloud with Microsoft Cloud App Security</title>
    </video>
    <video>
        <src>https://www.youtube.com/watch?v=goH_cgc7Nsw&list=PLXPr7gfUMmKxS1SYNgDaQY-9Q6cOqFxvG&index=13</src>
        <title>How to identify and protect overexposed data in the cloud with Microsoft Cloud App Security</title>
    </video>
<videoGroup>

## **Recommended Documents**

- [Session policies](https://docs.microsoft.com/cloud-app-security/session-policy-aad)
- [File policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies)
- [Sensitive information type entity definitions](https://docs.microsoft.com/microsoft-365/compliance/sensitive-information-type-entity-definitions)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
