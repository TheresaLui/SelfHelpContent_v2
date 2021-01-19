<properties
  pagetitle="Azure Policy - Guest Configuration policy compliance"
  service="microsoft.authorization"
  resource="policydefinitions"
  ms.author="migreene,kenieva"
  selfhelptype="Generic"
  supporttopicids="32741671"
  resourcetags=""
  productpesids="16456"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="fb8cb5a9-b9ee-4d95-8e4d-32537ce25c10"
  ownershipid="Compute_AzurePolicy" />
# Azure Policy - Guest Configuration policy compliance

**NOTE**: **Guest Configuration architecture was recently changed. For more information about the changes, please [click here](https://techcommunity.microsoft.com/t5/azure-governance-and-management/important-change-released-for-guest-configuration-audit-policies/ba-p/1655316)**.

For auditIfNotExists policies in the Guest Configuration category, there could be multiple settings evaluated inside the VM and you'll need to view per-setting details. For example, if you're auditing for a list of password policies and only one of them has status Non-compliant, you'll need to know which specific password policies are out of compliance and why.

The following documentation provides detailed information about how to view compliance details.

## **Recommended Documents**

- [Compliance details for Guest Configuration](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance#compliance-details-for-guest-configuration)
- [Understand Azure Policy's Guest Configuration](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration)
- [How to create Guest Configuration policies for Windows](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create)
- [How to create Guest Configuration policies for Linux](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create-linux)
- [Guest Configuration extension and client](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#extension-and-client)
