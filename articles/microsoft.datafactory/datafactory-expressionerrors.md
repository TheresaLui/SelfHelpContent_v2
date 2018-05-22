<properties 
	pageTitle="Data factory expression errors" 
	description="I get expression syntax or validation errors" 
	service="microsoft.datafactory" 
    resource="factories"
    authors="arthurw"
    displayOrder="16"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds="32605747"
    productPesIds="15613"
    resourceTags=""
/>

# Data Factory Expression Errors

## **Recommended steps**
- Although work is in progress to detect expression errors at authoring time in both UI experiences and create/update APIs, even simple typographical errors in expressions may cause errors at run time (when creating a pipeline run, or in monitoring responses for pipeline and activity runs).  Also, a syntax or validation error reported when running a pipeline may be due to an error in an expression in a dataset referenced by an activity in that pipeline, so it's important to check expressions carefully in all relevant entities.
- Be careful when using JSON within expressions, especially for arrays (even the data factory documentation sometimes gets this wrong and is being fixed).  For example, if you want to use a JSON array like [1, 2, 3] as the value of an expression in a ForEach activity, you can write expressions like "@json('[1,2,3]')" or "@createArray(1,2,3)" but <b>not</b> "@[1,2,3]".
- Only single quotes can be used within expressions (since the entire expression is within double quotes).  Single quotes can be escaped with an additional single quote, however it's easy to get wrong and may be hard to see depending on font.  For example the "one" in the following expression is within pairs of two single quotes (not a pair of double quotes): "@json('{''one'':1}').
- Consider testing expressions in small pipelines during development, especially using the "Debug" feature of the Data Factory authoring UI (documentation link below), so you can iterate quickly to find and fix expression-level issues before using the expression in a more complex context.

## **Recommended documents**
[Expression Language and Functions](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions/)<br>
[System Variables](https://docs.microsoft.com/azure/data-factory/control-flow-system-variables/)<br>
[Iterative Development and Debugging](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging/)
