<properties
    pageTitle="Guest Configuration extensions"
    description="Troubleshooting issues related to Guest Configuration extension"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="migreene"
    ms.author="migreene"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32743813"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="d54fd9a5-fe0a-45bf-9be9-f0092b29e5cf"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Guest Configuration extension and client

For Azure Policy to audit settings inside a machine, a
[virtual machine extension](https://docs.microsoft.com/azure/virtual-machines/extensions/overview)
is enabled. The extension downloads applicable policy assignment and the corresponding configuration definition.

The Guest Configuration extension is required to perform audits in Azure virtual machines. To
deploy the extension at scale, assign the following policy definitions:

- [Deploy prerequisites to enable Guest Configuration Policy on Windows VMs.](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2F0ecd903d-91e7-4726-83d3-a229d7f2e293)
- [Deploy prerequisites to enable Guest Configuration Policy on Linux VMs.](https://portal.azure.com/#blade/Microsoft_Azure_Policy/PolicyDetailBlade/definitionId/%2Fproviders%2FMicrosoft.Authorization%2FpolicyDefinitions%2Ffb27e9e0-526e-4ae1-89f2-a2a0bf0f8a50)

The following documentation provides details about Guest Configuration extension and client.

## **Recommended Documents**

- [Guest Configuration extension and client](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#extension-and-client)

### Related documents

- [Understand Azure Policy's Guest Configuration](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration)
- [How to create Guest Configuration policies for Windows](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create)
- [How to create Guest Configuration policies for Linux](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create-linux)
- [Compliance details for Guest Configuration](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance#compliance-details-for-guest-configuration)
