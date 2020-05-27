<properties
    pageTitle="Azure Security Center Recommendation - Recommendation keeps on appearing"
    description="Azure Security Center Recommendation - Recommendation keeps on appearing"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636900"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
     articleId="a15f057d-9111-9011-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Azure Security Center Recommendation - Recommendation keeps on appearing

## **Recommended Steps**

The given recommendation will be removed if one of the following conditions is true:

- All the resources under this recommendation become healthy.
- The recommendation is disabled through the Azure policy.

If you have followed the remediation steps, and the resource is still appearing as unhealthy, If you have followed the **Remediation** steps, and the resource is still showing as unhealthy, this issue can be caused by one of the following factors:

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

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)


