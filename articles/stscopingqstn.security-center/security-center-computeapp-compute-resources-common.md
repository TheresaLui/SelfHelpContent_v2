<properties
    pageTitle="Compute Resources Common Solutions"
    description="Compute Resources Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636867"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f057d-8uj6-4b97-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Compute Resources Common Solutions

Azure Security Center improves the security landscape by assessing your Azure services, and send recommendation based on security rules, our dashboard refresh for the assessment results, every 12 hours.

The services that we currently assess:

- Event Hub
- Service fabric
- Batch account
- Stream analytics
- Service bus
- Azure Search
- Logic app
- Automation account

We are consistently adding new recommendations to a new service.

## **Recommended Steps**

Azure Security Center uses Azure policy as the infrastructure for this recommendation, if you suspect that this recommendation doesn't present the real status of the service, refer the following steps:

1. Open Azure policy service
2. Open the Compliance
3. Select Azure Security Center Assignment. By default, the name is Enable Monitoring in Azure Security Center
4. Search the name of the policy you want to check, and select it
5. Check the compliance status for a given resource to see if the compliance state is Non-compliant
6. Press the context menu (the three dots in the end of the line), and choose the "view compliance detail"
7. Check for the "Reason for non-compliance", this will show the field that the policy is failed to be evaluated

## **Recommended Documents**

- [Azure Security Center Policies](https://docs.microsoft.com/azure/security-center/tutorial-security-policy)
- [Built-in Security Policies in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-policy-definitions)
- [Create and manage policies to enforce compliance](https://docs.microsoft.com/azure/governance/policy/tutorials/create-and-manage)
- [Overview of the Azure Policy service](https://docs.microsoft.com/azure/governance/policy/overview)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)