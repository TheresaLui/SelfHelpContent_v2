<properties
  pagetitle="Azure Pipelines issues related to YAML, conditions, and expressions&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="macoope,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742334"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesyaml"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines issues related to YAML, conditions, and expressions

Use the following recommendations to resolve common issues related to Azure Pipelines YAML, conditions, or expressions.

## **Recommended Steps**

Review each of the following steps before you create a support ticket. If you need to create a ticket, provide information about the path you took and the results of the steps you ran to expedite the resolution of your problem.

**I'm getting an error about unexpected mappings, sequences, scalars, or keys**

  - To write an Azure Pipelines YAML pipeline, an understanding of basic YAML syntax is required. You can find many tutorials available online, for example, [Learn YAML in Y minutes](https://learnxinyminutes.com/docs/yaml/).
  - Azure Pipelines doesn't support YAML anchors, tags (custom types), or binary data
  - After you understand the rules for a syntactically-correct YAML document, you can better understand the [Azure Pipelines schema](https://docs.microsoft.com/azure/devops/pipelines/yaml-schema) for defining pipelines

**I'm getting an error about exceeding one or more limits**

  - Azure Pipelines defines [limits](https://docs.microsoft.com/azure/devops/pipelines/process/templates#imposed-limits) on how much memory, how many files, and how deeply-nested a YAML pipeline can be. These limits protect the service as well as help you catch some classes of errors, such as infinite loops or mutually-recursive nesting.
  - Reduce the size, number of included files, or nesting depth of your pipeline if you encounter one of these limits

**My condition or expression isn't working the way I expect**

  - Expressions are written in a prefix-based, loosely-typed, pure-functional language. Functions are written as `functionname(arguments)`.
  - Functions are executed from the innermost parentheses and working outward. Therefore, in the expression `func1(func2(somevalue))`, first `func2(somevalue)` is computed. Then, the result of that computation is passed as the argument to `func1`.
  - Function arguments are evaluated left to right with short-circuiting. Therefore, in the expression `or(func1(), func2())`, if `func1` results in `True`, `func2` will not be evaluated.
  - Because the language is loosely-typed, functions may coerce their arguments to different data types silently. These coercions are documented as [typecasts](https://docs.microsoft.com/azure/devops/pipelines/process/expressions#type-casting).
  - Variables are always treated as strings. Be careful when testing variables in a Boolean context. Empty strings are `False` and non-empty strings are `True`. The correct way to test a variable for its Boolean value is to do a string comparison: `eq(variables.MyVar, 'false')`.

**I added a custom condition and now my step/job/stages is being skipped (or run) when I don't expect it**

  - By default, all stages, jobs, and steps act as if they have `condition: succeeded()`
  - If you add a custom condition, this implicit default will no longer apply. For example, if you write `condition: eq(variables['Build.SourceBranch'], 'refs/heads/main')` for a job, the job will run whenever the `main` branch triggers the pipeline, even if a previous job failed.
  - To retain the implied behavior, use a logical AND: `condition: and(succeeded(), <your custom condition>)`

## **Recommended Documents**

* [YAML schema](https://docs.microsoft.com/azure/devops/pipelines/yaml-schema)
* [Expressions](https://docs.microsoft.com/azure/devops/pipelines/process/expressions)
* [Conditions](https://docs.microsoft.com/azure/devops/pipelines/process/conditions)
* [Troubleshoot pipelines](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
