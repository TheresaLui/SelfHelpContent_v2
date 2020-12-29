<properties
  pagetitle="Azure Policy - My problem is not listed here"
  service="microsoft.authorization"
  resource="policydefinitions"
  ms.author="robga,kenieva"
  selfhelptype="Generic"
  supporttopicids="32739636"
  resourcetags=""
  productpesids="16456"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="e47a6f09-5c90-46a5-ad54-c4a8d3e39136"
  ownershipid="Compute_AzurePolicy" />
# Azure Policy - My problem is not listed here
 
 ## **Recommended Steps**

* **Feature Requests**: The Azure Policy triages customers asks from [UserVoice](https://feedback.azure.com/forums/915958-azure-governance). Feel free to add in a new feature or vote on those already existing. 
* **Azure Policy and RBAC**: For information regarding the difference between Azure Policy and Azure Role Based Access Control, please refer [here](https://docs.microsoft.com/azure/governance/policy/overview#azure-policy-and-rbac).
* **Why are my resources not auto-remediating?**: Policy does not currently support auto-remediation. To remediate a resource, please start a remediation task, steps [here]( https://docs.microsoft.com/azure/governance/policy/how-to/remediate-resources).
* **How/When are compliance scans triggered?**: Please allow about 30 minutes for the compliance scan to be triggered and get back compliance results. Compliance scan is triggered once it receives notification of resource change and a new scan every 24 hours. If you do not see any results within 24 hours, please create a support ticket. You can trigger on demand scan using REST API and PS, information [here](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data#on-demand-evaluation-scan).
* **How do I find an alias?**: To search for an alias, you can run a command or use the VS Code extension. Steps [here](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition#find-the-property-alias).
* **How do I export my compliance data/ How do I export my policy definitions and assignments?**: We currently do not support exporting compliance data through the portal. Please leverage [UserVoice](https://feedback.azure.com/forums/915958-azure-governance?category_id=345055) to vote on your preference for exporting or other features. You can get compliance data through a [Rest API and/or Command line](https://docs.microsoft.com/azure/governance/policy/how-to/get-compliance-data) call. You can use our VS Code extension to export the definitions and assignments or our built-in export to Github button in the portal.
* **Can I use REGEX within Policy?**: We currently do not support REGEX handling, but it is currently under review. We continue to value your feedback and would appreciate getting more through our [UserVoice](https://feedback.azure.com/forums/915958-azure-governance?category_id=345055). This is a great way to vote on your preference for Regex handling or other features. An alternative for Regex handling is to leverage the [Value](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure#value) capability which helps you in checking conditions against parameters, template functions, or literals.
* **Why doesn't Modify work for my policy?**: [Modify](https://docs.microsoft.com/azure/governance/policy/concepts/effects#modify) is currently limited to select aliases. Current built-ins with the modify effect can be found in [built in policies](https://docs.microsoft.com/azure/governance/policy/samples/built-in-policies). 
* **How can I get information on what's to come for Azure Policy?**: If you are interested in getting more information on what the Azure Policy team is doing, join the quarterly call on Azure Governance [here](https://forms.office.com/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbRxn7UD7lweFDnmuLj72r6E1UN1dLNTBZUVMyNVpHUjJLRE5PVDVGNlkyOC4u)

## **Recommended Documents**

* [Policy Known Issues]( https://github.com/azure/azure-policy#known-issues)
* [Policy Common Issues]( https://docs.microsoft.com/azure/governance/policy/troubleshoot/general)
* [Tutorial for creating a custom policy](https://docs.microsoft.com/azure/governance/policy/tutorials/create-custom-policy-definition)
* [Understanding policy assignment](https://docs.microsoft.com/azure/governance/policy/concepts/assignment-structure)
* [Understanding policy definition](https://docs.microsoft.com/azure/governance/policy/concepts/definition-structure)
