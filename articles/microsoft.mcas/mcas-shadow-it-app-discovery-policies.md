<properties
  pageTitle="I'm having issues with Shadow IT or app discovery policies"
  description="I'm having issues with Shadow IT or app discovery policies"
  infoBubbleText=""
  service="microsoft.Cloud App Security"
  resource=""
  authors="shsagir"
  ms.author="shsagir"
  displayOrder=""
  articleId="mcas-shadow-it-app-discovery-policies"
  diagnosticScenario=""
  selfHelpType="generic"
  supportTopicIds="32729003"
  resourceTags=""
  productPesIds="16031"
 ownershipId="CloudAppSecurity_Discovery"
  cloudEnvironments="public, fairfax, usnat, ussec"
/>

# I'm having issues with Shadow IT or app discovery policies

Most users are able to resolve Shadow IT or app discovery policy issues using the steps below.

## **Recommended Steps**

1. Use the steps in [Export a block script to govern discovered apps](https://docs.microsoft.com/cloud-app-security/governance-discovery#export-a-block-script-to-govern-discovered-apps) to configure block script for on-premises security appliances.
    1. Generate a list of domains for all apps that were marked as unsanctioned in Cloud App Security.
    1. Use the list to populate your enforcing appliances, such as a Secure Web Gateway (SWG), proxy server, or firewall to block the required apps.
1. Use the steps in [Evaluate and analyze](https://docs.microsoft.com/cloud-app-security/tutorial-shadow-it#phase-2-evaluate-and-analyze) to get notified when a discovered app is associated with a recently published security breach using the built-in **Discovered app security breach** alert. Investigate all users, IP addresses, and devices accessing the breached app in the last 90 days, and apply relevant controls.
1. Configure risk scores to adapt Cloud App Security to your organization's requirements. By default, Cloud App Security analysts continuously update app risk indicators that affect an app's general risk score. You can customize risk scores or their indicators, as follows:
    1. You can [submit change suggestions](https://docs.microsoft.com/cloud-app-security/risk-score#suggesting-a-change) to risk scores or specific risk factors for approval by Cloud App Security analysts.
    1. You can [customize](https://docs.microsoft.com/cloud-app-security/risk-score#customizing-the-risk-score) an app's risk score.
1. Add [custom apps](https://docs.microsoft.com/cloud-app-security/cloud-discovery-custom-apps) to enable the detection of line-of-business apps to the Cloud App Catalog.

    **IMPORTANT**  
    When setting up custom apps, make sure that all domains and related IP addresses are configured to ensure apps are correctly identified.
1. [Enrich Cloud Discovery](https://docs.microsoft.com/cloud-app-security/cloud-discovery-aad-enrichment) data with Azure Active Directory (AD) username based on the user's Unique Principal Name from Azure AD. Doing so provides a better investigation experience.

## **Recommended Documents**

- [Tutorial: Discover and manage shadow IT in your network](https://docs.microsoft.com/cloud-app-security/tutorial-shadow-it)
- [Troubleshooting Cloud Discovery](https://docs.microsoft.com/cloud-app-security/troubleshooting-cloud-discovery)
- [Working with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps)
- [Set up Cloud Discovery](https://docs.microsoft.com/cloud-app-security/set-up-cloud-discovery)
- [Cloud Discovery policies](https://docs.microsoft.com/cloud-app-security/cloud-discovery-policies)
- [Govern discovered apps](https://docs.microsoft.com/cloud-app-security/governance-discovery)

If you're still experiencing the issue after reviewing the documentation and configuration, please continue with opening the ticket.
