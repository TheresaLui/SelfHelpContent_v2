<properties
    pageTitle="Compliance state and details not as expected"
    description="Compliance state and details not as expected"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739633"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="34a89633-83f9-4b52-a866-d9415078d9cd"
    ownershipId="Compute_AzurePolicy"
/>

# Azure Policy - Compliance state and details not as expected

## **Recommended Steps**

* **Understanding compliance scan**

During an initial compliance scan, the policy compliance engine will search for all existing resources in that scope (i.e. If the type is storage accounts, then the engine will search for all storage accounts in that scope). Once the targeted resources are discovered, the engine will check for compliance to the definition. If the resource does not meet the requirements (does not meet the 'if'), then it will be marked as [non-compliant](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance). All new and existing resources will be marked either compliant or non-compliant.
After the initial scan, policy engine will have another full scan every 24 hours and delta scans when a resource change is detected. More on getting compliance data [here](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data).

* **Triggering azure policy compliance**

The first compliance scan can take time to be triggered in which it will be in 'Not Started' phase. Please allow about _30 minutes_ for  compliance results. Compliance scan is triggered once it receives notification of resource change and a new scan every 24 hours. If you do not see any results within 24 hours, please create a support ticket.
You can trigger an on demand scan using REST API and PowerShell, please refer [here](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data#on-demand-evaluation-scan).

* **Compliance not correct/not as expected debugging**

If your compliance is not correct/ not as expected, please check the compliance details. Ensure the expected results are correct and modify the definition or assignment as needed.  If this is a built-in policy, be sure to have the correct parameters and the assignment is to the correct scope.
If your compliance shows 0/0 resources, this is because the policy compliance didn't find any resources that match your definition. Please revise your definition.
Keep in mind that for deployIfNotExist and Modify policies, existing resources will not be automatically remediated. You need to create a remediation task.
To find help with definition debugging a policy, please refer to support topics section: Authoring a policy.

* **Azure Security Center policies compliance**

Azure Security Center's (ASC) policies are built on top of the Azure Policy platform. However, ASC policies have their own management, hence we recommend managing ASC policies on ASC. Policy does not evaluate ASC resources but just report back information from the Microsoft.Security Resource Provider. Therefore, if the compliance of ASC Policies are not correct, please route your questions to ASC.

## **Recommended Documents**

* [Get compliance data](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data)
* [How are arrays evaluated](https://docs.microsoft.com/azure/governance/policy/how-to/author-policies-for-arrays)
* [Determine causes of non-compliance](https://docs.microsoft.com/azure/governance/policy/how-to/determine-non-compliance)
* [Understanding policy definition](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
* [Understanding policy effects](https://docs.microsoft.com/azure/governance/policy/concepts/effects)
* [Evaluate impact of a new policy](https://docs.microsoft.com/azure/governance/policy/concepts/evaluate-impact)
