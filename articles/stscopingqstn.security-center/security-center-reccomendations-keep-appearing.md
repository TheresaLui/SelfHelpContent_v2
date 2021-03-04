<properties
  pagetitle="Azure Security Center Recommendation - Recommendation keeps on appearing&#xD;"
  description="Azure Security Center Recommendation - Recommendation keeps on appearing"
  ms.author="elsagie"
  selfhelptype="Generic"
  supporttopicids="32788547,32788549,32788551,32788555,32788557,32788558"
  resourcetags=""
  productpesids="15947"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a15f057d-9111-9011-a98a-dfaf3843dc2f"
  ownershipid="Azure_Security_Security_Center" />
# Azure Security Center Recommendation - Recommendation keeps on appearing

If recommendations keep appearing in the Azure Security Center, follow these steps. <br>
Recommendations are removed if one of the following conditions is true:

- All the resources under this recommendation become healthy
- The recommendation is disabled through the Azure policy


## **Recommended Steps**

If you have followed the remediation steps, and the resource is still appearing as unhealthy, it may be due to one of the following factors:

- The Recommendations is not refreshed. Recommendations refresh every 12 hours.

- The Security Center has not received the new data from the Operations Management Suite (OMS) agent in the VM. For more information, see [How often does Security Center scan for operating system](https://docs.microsoft.com/azure/security-center/security-center-faq#how-often-does-security-center-scan-for-operating-system-vulnerabilities-system-updates-and-endpoint-protection-issues)

- In addition, Security Center uses Azure policy as its main policy engine. Check the recommendation status in Azure Policy compliance center:

   1. Open Azure policy in Azure portal
   2. Open the **Compliance** view
   3. Go to Azure Security Center default assignments on the subscription or management group level
   4. Search for the relevant recommendation
   5. Validate if the resource is compliant

## **Recommended Documents**

- [Managing security recommendations in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-recommendations)
- [Use Azure Security Center recommendations to enhance security](https://docs.microsoft.com/azure/security-center/security-center-using-recommendations)
- [How to Strengthen your security posture with Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-monitoring)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)
