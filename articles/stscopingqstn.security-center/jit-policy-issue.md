<properties
    pageTitle="JIT Policy issue"
    description="Details of the JIT Policy issue"
    service=""
    resource=""
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    authorAlias="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680776"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="4abffa62-1bf2-49d6-b4f7-5aafbd02a598"
	ownershipId="Azure_Security_Security_Center"
/>

# JIT Policy issue

When a virtual machine (VM) is first configured to Just in Time (JIT), a policy is created defining the following parameters:

* PORT
* PROTOCOL
* ALLOWED SOURCE IPS
* IP RANGE
* TIME RANGE (HOURS)

After creating the policy, you can edit each one per VM from the **Security Center portal – Just in time VM** access blade.

### Using the Set-AzJitNetworkAccessPolicy PowerShell cmdlet

* When creating a new policy using PowerShell, the name must be set to "default"
* For any additional VMs that you want to add after first policy was set, you must create an array for all configured VMs. Otherwise, the current policy will override the existing "default" policy.

We are going to improve this behavior in the future.

## **Recommended Documents**

* [Manage virtual machine access using Just-in-time](https://docs.microsoft.com/azure/security-center/security-center-just-in-time)<br>
* [How to configure Just-in-time](https://docs.microsoft.com/azure/security-center/tutorial-protect-resources)
