<properties
    pageTitle="Remediation task behavior not as expected"
    description="Assistance with remediation task"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="kenieva"
    ms.author="kenieva"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32741672"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="b3344bfb-13b6-4348-aa55-01b6700530e1"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Remediation task behavior not as expected

## **Recommended Steps**

* **Permissions**: If you are creating the remediation through a command, be sure that the managed identity has the proper permissions. Contributor role is not enough. 
1- Managed identity does not have permissions. Portal no worries. 
If not using portal, create role assignments manually and give permission. Contributor role is not enough. Follow this tutorial: [here](https://docs.microsoft.com/azure/governance/policy/how-to/remediate-resources#manually-configure-the-managed-identity)

* **Modify Tags Known Issues**: There are some known issues, please check [here](https://github.com/Azure/azure-policy#known-issues). We are working to solve these.
In the meantime you can [exclude](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure#excluded-scopes) those resources. 

* **DeployIfNotExist Failing**- Please verify that the ARM template works. For information on ARM templates, check [here](https://docs.microsoft.com/azure/azure-resource-manager/templates/overview) 
## **Recommended Documents**

* [Remediate non-compliant resources](https://docs.microsoft.com/azure/governance/policy/how-to/remediate-resources)
* [Modify effect](https://docs.microsoft.com/azure/governance/policy/concepts/effects#modify)
* [DeployIfNotExist effect](https://docs.microsoft.com/azure/governance/policy/concepts/effects#deployifnotexists)
* [PowerShell Remediation Commands](https://docs.microsoft.com/powershell/module/az.policyinsights/?view=azps-4.1.0#policy_insights)
* [Rest API Remediation Commands](https://docs.microsoft.com/rest/api/policy-insights/remediations)


