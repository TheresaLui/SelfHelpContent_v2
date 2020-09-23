<properties
	pageTitle="Pipelines retention"
	description="Azure Pipelines issues related to retention"
	infoBubbleText="Azure Pipelines issues related to retention"
	service="microsoft.visualstudio"
	resource="account"
	authors="vijayma"
	ms.author="vijayma"
	articleId="AZDevOpsPipelinesRetentionIssues"
	supportTopicIds="32742327"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines Retention Issues

## **Recommended Steps**

Are you facing one of these common problems?

* I lost some of the pipeline runs. Is there a way to get them back?

  - Understand how retention works and when runs are deleted by reviewing the [docs](https://docs.microsoft.com/azure/devops/pipelines/policies/retention?view=azure-devops&tabs=yaml#set-run-retention-policies).
  - If you believe that you have lost the runs due to a bug in the service, then create a support ticket to recover the lost information. 
  - If the runs have been deleted as expected due to a retention policy or if the runs have been deleted more than a week ago, then it is not possible to recover the lost runs.

* We need to retain builds and releases longer than what is allowed in the settings. How can I request a longer retention?

  - There is no way to configure a longer retention setting in Azure DevOps.
  - One way to retain a run or a release longer than what is allowed through retention settings is to manually mark it to be retained indefinitely. Such runs will stay in the system until you delete them manually.
  - You can also copy artifacts to your [own storage](https://docs.microsoft.com/azure/devops/pipelines/policies/retention?view=azure-devops&tabs=yaml#use-the-copy-files-task-to-save-data-longer) in order to keep them longer.

## **Recommended Documents**

* [Retention settings for classic build and YAML pipelines](https://docs.microsoft.com/azure/devops/pipelines/policies/retention?view=azure-devops&tabs=yaml#set-run-retention-policies)
* [Retention settings for classic release pipelines](https://docs.microsoft.com/azure/devops/pipelines/policies/retention?view=azure-devops&tabs=yaml#set-release-retention-policies)
* [Retention settings for manual tests](https://docs.microsoft.com/azure/devops/pipelines/policies/retention?view=azure-devops&tabs=yaml#set-test-retention-policies)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)