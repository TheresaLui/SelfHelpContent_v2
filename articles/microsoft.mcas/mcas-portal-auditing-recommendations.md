<properties
  pageTitle="I'm having problems viewing security auditing, security recommendations, or compliance status for Azure, AWS, or GCP"
  description="I'm having problems viewing security auditing, security recommendations, or compliance status for Azure, AWS, or GCP"
  infoBubbleText=""
  service="microsoft.mcas"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-portal-auditing-recommendations"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32728965"
  resourceTags=""
  productPesIds="16031"
  ownershipId="CloudAppSecurity_API"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having problems viewing security auditing, security recommendations, or compliance status for Azure, AWS, or GCP

Most users are able to solve viewing security auditing, security recommendations, or compliance status issues using the steps below.

## **Recommended Steps**

If you need help with protecting Azure, make sure that you have:

- [Connected your Azure tenant to Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-azure-to-microsoft-cloud-app-security)
- Enabled [Azure Security Center](https://docs.microsoft.com/cloud-app-security/security-config-azure#how-to-enable-azure-security-recommendations) (free or standard tiers) and view the recommendations in the ASC console

### Protecting AWS

For AWS security auditing, make sure that you have:

- Configured [AWS auditing](https://docs.microsoft.com/cloud-app-security/connect-aws-to-microsoft-cloud-app-security#step-1-configure-amazon-web-services-auditing)
- Connected your [AWS accounts for security auditing to Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-aws-to-microsoft-cloud-app-security#step-2-connect-amazon-web-services-auditing-to-cloud-app-security)
- For AWS security recommendations, make sure that you have:

  - Configured [AWS Security Hub and view the recommendations in the Security Hub](https://docs.microsoft.com/cloud-app-security/connect-aws-to-microsoft-cloud-app-security#set-up-aws-security-hub)
  - Connected your [AWS accounts for security recommendations to Cloud app security](https://docs.microsoft.com/cloud-app-security/connect-aws-to-microsoft-cloud-app-security#connect-aws-security-configuration-to-cloud-app-security)

### Protecting GCP

For GCP security auditing, make sure that you have:

  - Configured [GCP auditing](https://docs.microsoft.com/cloud-app-security/connect-google-gcp-to-microsoft-cloud-app-security#configure-google-cloud-platform)
  - Connected your [GCP organization for security auditing to Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-google-gcp-to-microsoft-cloud-app-security#connect-google-cloud-platform-auditing-to-cloud-app-security)

- For GCP security recommendations, make sure that you have:

  - Configured [GCP Security and Command Center with Security Health Analytics](https://docs.microsoft.com/cloud-app-security/connect-google-gcp-to-microsoft-cloud-app-security#set-up-gcp-security-command-center-with-security-health-analytics)
  - Connected your [GCP organization for security recommendations to Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-google-gcp-to-microsoft-cloud-app-security#connect-google-cloud-platform-security-configuration-to-cloud-app-security)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
