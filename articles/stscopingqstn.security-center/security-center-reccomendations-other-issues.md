<properties
    pageTitle="Azure Security Center Recommendation - Other Issues Common Solutions"
    description="Azure Security Center Recommendation - Other Issues Common Solutions"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636902"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f057d-9001-8010-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Azure Security Center Recommendation - Other Issues Common Solutions"

## **Recommended Steps**

**A given recommendation disappears from Security Center**

Azure Security Center periodically analyzes the security state of your Azure resources. When Azure Security Center identifies potential security vulnerabilities, it creates recommendations.

The given recommendation will be removed if one of the following conditions is true:

- All the resources under this recommendation become healthy.
- The recommendation is disable from the Azure policy.

If you have followed the **Remediation** steps, and the resource is still showing as unhealthy, this issue can be caused by one of the following factors:

- The Recommendations is not refreshed. The Recommendations are refreshed every 12 hours.
- The security Center has not received the new data from the Operations Management Suite (OMS) agent in the VM. For more information, see [How often does Security Center scan for operating system](https://docs.microsoft.com/azure/security-center/security-center-faq#how-often-does-security-center-scan-for-operating-system-vulnerabilities-system-updates-and-endpoint-protection-issues)

In addition, Azure security center uses Azure policy as its main policy engine. Check the recommendation status in Azure Policy compliance center, to do so please, follow these steps:

1. Open Azure policy in Azure portal.
2. Open the Compliance view.
3. Go to Azure security center default assignments. It is on the subscription or management group level.
4. Search for the relevant recommendation.
5. Validate if the resource is compliance or not.

## **Recommended Documents**

- [Managing security recommendations in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-recommendations)
- [Use Azure Security Center recommendations to enhance security](https://docs.microsoft.com/azure/security-center/security-center-using-recommendations)
- [How to Strengthen your security posture with Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-monitoring)

**Troubleshooting**

-[Azure Security Center Troubleshooting Guide] https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide

**FAQ**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**How to and advisory information**

- [Azure Security Center Pricing Tiers](https://docs.microsoft.com/azure/security-center/security-center-pricing)
- [Azure Security Center Readiness Roadmap](https://docs.microsoft.com/azure/security-center/security-center-readiness-roadmap)
- [Permissions in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-permissions)
- [Azure Security Center REST API](https://docs.microsoft.com/rest/api/securitycenter/)
- [Check out our latest Azure Security Center updates](https://azure.microsoft.com/updates/?product=security-center)

