<properties
    pageTitle="Guest Configuration policy compliance"
    description="Understanding how to view the details of compliance for settings inside machines"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="migreene"
    ms.author="migreene"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32741669,32741670,32741671"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="a53d0830-04c0-4b16-a51c-9a089a0337f5"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Guest Configuration policy compliance

For auditIfNotExists policies in the Guest Configuration category, there could be multiple settings evaluated inside the VM and you'll need to view per-setting details. For example, if you're auditing for a list of password policies and only one of them has status Non-compliant, you'll need to know which specific password policies are out of compliance and why.

The following documentation provides detailed information about how to view compliance details.

## **Recommended Documents**

- [Compliance details for Guest Configuration](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance#compliance-details-for-guest-configuration)

### Related documents

- [Understand Azure Policy's Guest Configuration](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration)
- [How to create Guest Configuration policies for Windows](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create)
- [How to create Guest Configuration policies for Linux](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create-linux)
- [Guest Configuration extension and client](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#extension-and-client)
