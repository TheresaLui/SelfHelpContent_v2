<properties
    pageTitle="Guest Configuration policies"
    description="Working with policies for governing settings inside virtual machines"
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

# Azure Policy - Using Guest Configuration policies

Azure Policy can audit settings inside a machine. The validation is performed by the Guest Configuration extension and client. The extension, through the client, validates settings such as:

- The configuration of the operating system
- Application configuration or presence
- Environment settings

At this time, most Azure Policy Guest Configuration policies only audit settings inside the machine. They don't apply configurations.

The following documentation provides details about Guest Configuration policies.

## **Recommended Documents**

- [Understand Azure Policy's Guest Configuration](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration)

### Related documents

- [How to create Guest Configuration policies for Windows](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create)
- [How to create Guest Configuration policies for Linux](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create-linux)
- [Compliance details for Guest Configuration](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance#compliance-details-for-guest-configuration)
- [Guest Configuration extension and client](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#extension-and-client)
