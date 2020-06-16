<properties
    pageTitle="Guest Configuration custom policies"
    description="Creating custom policies for Azure Policy Guest Configuration"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="migreene"
    ms.author="migreene"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32741670"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="a53d0830-04c0-4b16-a51c-9a089a0337f5"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Guest Configuration custom policies

When auditing Windows, Guest Configuration uses a
[Desired State Configuration](https://docs.microsoft.com/en-us/powershell/scripting/dsc/overview/overview)
(DSC) resource module to create the configuration file. The DSC configuration defines the condition that the machine should be in. If the evaluation of the configuration fails, the policy effect auditIfNotExists is triggered and the machine is considered non-compliant.

When auditing Linux, Guest Configuration uses
[Chef InSpec](https://www.inspec.io/).
The InSpec profile defines the condition that the machine should be in. If the evaluation of the configuration fails, the policy effect auditIfNotExists is triggered and the machine is considered non-compliant.

Before creating custom policy definitions, it's a good idea to read the
[conceptual overview information](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration).

The documentation below provides detailed information regarding custom policies for Windows and Linux machines.

## **Recommended Documents**

- [How to create Guest Configuration policies for Windows](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create)
- [How to create Guest Configuration policies for Linux](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create-linux)

### Related documents

- [Understand Azure Policy's Guest Configuration](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration)
- [Compliance details for Guest Configuration](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance#compliance-details-for-guest-configuration)
- [Guest Configuration extension and client](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#extension-and-client)
