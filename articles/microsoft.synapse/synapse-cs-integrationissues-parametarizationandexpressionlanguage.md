<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783897"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Integration Issues/Parametarization and expression language"
    description = "Integration Issues/Parametarization and expression language"
    articleId = "synapse-cs-integrationissues-parametarizationandexpressionlanguage.md"
    ms.author = "saltug"
/>

# Integration Issues/Parametarization and expression language

## **Recommended Steps**

* Please note that even simple typographical errors in expressions may cause errors at run time

* A syntax or validation error reported during runtime can be caused by an expression error in dataset setting and/or activity definition referenced in the pipeline. So it's important to check expressions carefully in all relevant entities

* Please be extra careful when writing JSON within expressions, particularly when using arrays types. For example, if you want to use a JSON array, like [1, 2, 3], as the value of an expression in a ForEach activity, you can write expressions "@json('[1,2,3]')" or "@createArray(1,2,3)", but not "@[1,2,3]"

* Only single quotes can be used within expressions, while double quotes are reserved to mark the ends of the entire expression. Single quotes can be escaped with an additional single quote, however it's may be hard to see depending on font and easy to get wrong. Please use extra caution when leveraging these capabilities. For example, one in following expression is within pairs of two single quotes (not a pair of double quotes): "@json('{''one'':1}')".

* Consider testing expressions in small pipelines during development, so you can iterate quickly to find and fix expression-level issues before using the expression in a more complex context. Please consider utilize the "Debug" mode in ADF portal experience. See [Iterative Development and Debugging](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json)

## **Recommended Documents**

* Build dynamic contents with [functions and parameters](https://docs.microsoft.com/azure/data-factory/author-visually?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#expressions-and-functions)

* [Expression Language](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json)

* [System Variables](https://docs.microsoft.com/azure/data-factory/control-flow-system-variables?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json)

* [Functions](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#functions) including:

* [String](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#string-functions) functions only apply to strings

* [Collection](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#collection-functions) functions operate over collections, such as arrays, strings, and in some cases dictionaries

* [Logical](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#logical-functions) functions are useful inside conditions

* [Conversion](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#conversion-functions) functions convert between native types

* [Math](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#math-functions) functions are used for either integer or float

* [Date](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json#date-functions) functions operate over timestamps

 