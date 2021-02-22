<properties
  pagetitle="Azure Policy - Guest Configuration extension and client"
  service="microsoft.authorization"
  resource="policydefinitions"
  ms.author="migreene,kenieva"
  selfhelptype="Generic"
  supporttopicids="32743813"
  resourcetags=""
  productpesids="16456"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="d54fd9a5-fe0a-45bf-9be9-f0092b29e5cf"
  ownershipid="Compute_AzurePolicy" />
# Azure Policy - Guest Configuration extension and client

**NOTE**: **Guest Configuration architecture was recently changed. For more information about the changes, [click here](https://techcommunity.microsoft.com/t5/azure-governance-and-management/important-change-released-for-guest-configuration-audit-policies/ba-p/1655316)**.

For Azure Policy to audit settings inside a machine, a [virtual machine extension](https://docs.microsoft.com/azure/virtual-machines/extensions/overview) is enabled. The extension downloads applicable policy assignment and the corresponding configuration definition.

The Guest Configuration extension is required to perform audits in Azure virtual machines. To deploy the extension at scale, assign the following policy definitions:

- [Deploy prerequisites to enable Guest Configuration Policy on Windows VMs](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F0ecd903d-91e7-4726-83d3-a229d7f2e293)
- [Deploy prerequisites to enable Guest Configuration Policy on Linux VMs](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Ffb27e9e0-526e-4ae1-89f2-a2a0bf0f8a50)

## **Recommended Documents**

* [User-assigned identities are overridden when system-assigned identities are provisioned](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#managed-identity-requirements)
* [Guest Configuration extension and client](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#extension-and-client)

In addition, all Guest Configuration policies that contain effect **DeployIfNotExist** and previously caused conflict with user-assigned identities are being marked as deprecated and replaced with new audit policies. This requires manually deleting existing policy assignments and assigning the new audit policies. For more information, see the [Guest Configuration Requirements](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#guest-configuration-definition-requirements).

- [Understand Azure Policy's Guest Configuration](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration)
- [How to create Guest Configuration policies for Windows](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create)
- [How to create Guest Configuration policies for Linux](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create-linux)
- [Compliance details for Guest Configuration](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance#compliance-details-for-guest-configuration)
