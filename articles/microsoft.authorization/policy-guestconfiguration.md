<properties
    pageTitle="Guest Configuration policies"
    description="Working with policies for governing settings inside virtual machines"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="migreene"
    ms.author="migreene"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32741669"
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

## Changes to definitions

During the month of August 2020, Guest Configuration policies will undergo a significant change. Customer feedback
has been that we should eliminate the need to run Remediation Tasks to enable Guest Configuration audits. To make this change,
we will create new **AuditIfNotExists** definitions with additional information in the metadata. The additional information is
used to automatically create resources in the `Microsoft.GuestConfiguration` Azure resource provider. This means that going forward,
a single Initiate can be used to enable all requirements for identity and extensions on a machine, and then audit policies
can be added/removed without needing to run Remediation Tasks.

The inititative to deploy requirements is named `Deploy prerequisites to enable Guest Configuration policies on virtual machines`. Once
it has been assigned (and any existing machines have been remediated), no additional "prerequisite" policies are required as
audit definitions are assigned.

All existing policies will be marked `[Deprecated]`. All policy assignments using the Initiatives and Definitions before this point in time
will continue to function normally.

The new policies will follow the name pattern `Audit <Windows/Linux> machines that <non-compliant condition>`. The new policies will
not require a built-in initiative.

Changing to the new policies is manual. There is no timeline for when the old policies would be deleted, to force the change to happen
by a specific date. When it is appropriate for your environmnt, you can assign the new definitions and delete any policy assignments you have that use the deprecated initatives/definitions. We appreciate your patience during this change.

## **Recommended Documents**

- [Understand Azure Policy's Guest Configuration](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration)

### Related Documents

- [How to create Guest Configuration policies for Windows](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create)
- [How to create Guest Configuration policies for Linux](https://docs.microsoft.com/azure/governance/policy/how-to/guest-configuration-create-linux)
- [Compliance details for Guest Configuration](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance#compliance-details-for-guest-configuration)
- [Guest Configuration extension and client](https://docs.microsoft.com/azure/governance/policy/concepts/guest-configuration#extension-and-client)
