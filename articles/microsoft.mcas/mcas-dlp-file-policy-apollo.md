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
  supportTopicIds="9f3fa90f-696f-1a7b-0b50-81317185ecfb"
  productPesIds="16031"
  cloudEnvironments="public"
  ownershipId="CloudAppSecurity_DataProtection"
/>

# Welcome to our new guided troubleshooting experience for DLP and file policies

## Troubleshooting DLP and file policies for Cloud App Security

Follow the recommended steps and how-to videos based on the issue you are having with DLP and file policy.

:::Section Recommended Solution:::

### Recommended solutions for commonly occuring issues

1. If you're sharing files and the domain isn't detected: 
- This can occur when sharing files with external users who are using a group and the Collaborators filter is set to "Any from domain." In this setup, domains are not detected for members of a group and can be detected only for users who have direct permissions on the file.
2. If your data classification service sensitive types aren't matching as expected: 
- Review the conditions of each [sensitivity type](https://docs.microsoft.com/microsoft-365/compliance/sensitive-information-type-entity-definitions), and in the advanced settings, verify that each sensitive type matches accuracy and that instance counts are configured correctly.
3. If you are unable to investigate and control files:
- Verify that file monitoring is enabled. In Cloud App Security, select **Settings** > **Files**, and then click **Enable file monitoring**. If you don't have access to the *Files* page for more than 60 days and have no active file policies, file monitoring will be automatically disabled. Learn more about [Labels, Sensitive Information Types and Microsoft Information Protection](https://techcommunity.microsoft.com/t5/core-infrastructure-and-security/a-journey-to-holistic-cloud-protection-with-the-microsoft-365/ba-p/1341515).

### Learn about protecting your data by using the how-to videos below:

<videoGroup>
    <video>
        <src>https://www.youtube.com/watch?v=ZY1n7b29KtE&list=PLXPr7gfUMmKxS1SYNgDaQY-9Q6cOqFxvG&index=12</src>
        <title>How to label and protect all your data in the cloud with Microsoft Cloud App Security</title>
    </video>
    <video>
        <src>https://www.youtube.com/watch?v=goH_cgc7Nsw&list=PLXPr7gfUMmKxS1SYNgDaQY-9Q6cOqFxvG&index=13</src>
        <title>How to identify and protect overexposed data in the cloud with Microsoft Cloud App Security</title>
    </video>
</videoGroup>

### More resources

- [Session policies](https://docs.microsoft.com/cloud-app-security/session-policy-aad)
- [File policies](https://docs.microsoft.com/cloud-app-security/data-protection-policies)
- [Sensitive information type entity definitions](https://docs.microsoft.com/microsoft-365/compliance/sensitive-information-type-entity-definitions)
