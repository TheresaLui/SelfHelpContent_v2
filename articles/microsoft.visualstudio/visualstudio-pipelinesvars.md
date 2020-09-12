<properties
  pagetitle="Variables and parameters"
  description="Azure Pipelines issues related to variables and parameters"
	infoBubbleText="Azure Pipelines issues related to variables and parameters"
	service="microsoft.visualstudio"
  resource="account"
  ms.author="macoope"
  selfhelptype="Generic"
  supporttopicids="32742333"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="AZDevOpsPipelinesVars"
  ownershipid="Azure_DevOps_Services" />

# Azure Pipelines issues related to variables and parameters

## **Recommended Steps**

You may be having trouble related to variables or parameters in Azure Pipelines.

Follow through all the steps before you create a support ticket. If you do need to create a ticket after completing the diagnostic steps, provide information about the path you took and results of the steps you ran in your ticket to expedite the resolution of your problem.

**I want to share variables across pipelines.**

  - Azure Pipelines allows sharing variables using [variable groups](https://docs.microsoft.com/azure/devops/pipelines/library/variable-groups)
  - YAML pipelines can also take advantage of [variable templates](https://docs.microsoft.com/azure/devops/pipelines/process/templates#variable-reuse)

**I want to set pipeline variables at runtime.**

  - Azure Pipelines has a [logging command language](https://docs.microsoft.com/azure/devops/pipelines/scripts/logging-commands) which you can use to request runtime changes
  - You can use the [`setvariable` command](https://docs.microsoft.com/azure/devops/pipelines/scripts/logging-commands#setvariable-initialize-or-modify-the-value-of-a-variable) to create new pipeline variables

**I want to set specific environment variables, but their names are always transformed to uppercase.**

  - Azure Pipelines distinguishes between [pipeline variables](https://docs.microsoft.com/azure/devops/pipelines/process/variables) and environment variables
  - Pipeline variables are made available as environment variables. Their names are always transformed to uppercase and periods are replaced with underscores.
  - Pipeline variables can be set at the definition, stage, or job level.
  - Individual steps can have environment variables. These variables do not have their names transformed. Environment variables can be set in the step editor for classic Build pipelines, or using the [`env` keyword](https://docs.microsoft.com/azure/devops/pipelines/yaml-schema#steps) in YAML pipelines.

**I want to use a variable in a template expression (`${{ }}`).**

  - Template expressions are resolved before the pipeline begins running. Read more about [how pipelines are processed](https://docs.microsoft.com/azure/devops/pipelines/process/runs#process-the-pipeline).
  - Only some variables are in scope when template expressions are processed. These are documented in the [predefined variables](https://docs.microsoft.com/azure/devops/pipelines/build/variables) topic.
  - Variables you define at runtime, variables defined in the UI, and variables not at global scope within YAML are not available during template expression processing

**I want to depend on variables produced in another job, or in another stage.**

  - YAML pipelines can depend on output variables produced elsewhere in the pipeline
  - You must declare the jobs or stages you depend on. Then, you can use the [`dependencies` and `stageDepdencies` keywords](https://docs.microsoft.com/azure/devops/pipelines/process/expressions#dependencies).
  - Pay close attention to the syntax. In particular, cross-stage dependencies have a different syntax depending on whether you're consuming them at a stage level or job level.

## **Recommended Documents**

* [Troubleshoot pipelines](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)
