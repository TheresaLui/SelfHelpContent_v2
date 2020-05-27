<properties
    pageTitle="Compliance state and details"
    description="Compliance state and details"
    service="microsoft.authorization"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32730241"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="97726c01-5bc5-40cf-8a04-fe6204ca247d"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Compliance state and details

## **Recommended Steps**

* **Understanding compliance scan**

During an initial compliance scan, the policy compliance engine will search for all existing resources in that scope (i.e. If the type is storage accounts, then the engine will search for all storage accounts in that scope). Once the targeted resources are discovered, the engine will check for compliance to the definition. If the resource does not meet the requirements (does not meet the "if"), then it will be marked as non-compliant. All new and existing resources will be marked either compliant or [non-compliant](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance).
After the initial scan, policy engine will have another full scan every 24 hours and delta scans when a resource change is detected. More on getting compliance data [here](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data).

* **Triggering azure policy compliance**

The first compliance scan can take time to be triggered in which it will be in "Not Started" phase. Please allow about 15 minutes for the compliance scan to be triggered and get back compliance results. Compliance scan is triggered once it receives notification of resource change and a new scan every 24 hours. If you do not see any results within 24 hours, please create a support ticket. 
To get information on demand scan, please refer [here](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data#on-demand-evaluation-scan).

* **Compliance not correct/not as expected**

If your compliance is not correct/ not as expected, please check the definition. Sometimes the definition is not targeting the correct resource type. You can do this by checking the [alias](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias).  If this is a built-in policy, be sure to have the correct parameters and the assignment is to the correct scope.
For more help with definitions, please change the support topic to "Authoring a custom policy".

## **Recommended Documents**

* [Get compliance data](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data)
* [How are arrays evaluated](https://docs.microsoft.com/azure/governance/policy/how-to/author-policies-for-arrays)
* [Determine causes of non-compliance](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
* [Understanding policy definition](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
* [Understanding policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)
* [Evaluate impact of a new policy](https://docs.microsoft.com/azure/governance/policy/concepts/evaluate-impact) 
