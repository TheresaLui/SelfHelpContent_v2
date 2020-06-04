<properties
	pageTitle="Use Expression and Functions to Build Dynamic Contents"
	description="Expressions and functions in Azure Data Factory"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="283d9e5d-d00f-47df-8c3d-0db4deda2903"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629484"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Expressions and Functions

## **Recommended Steps**

* Recently, ADF has added some validations capabilities in ADF portal experience to detect common expression errors <br>
* Please note that even simple typographical errors in expressions may cause errors at run time <br>
* A syntax or validation error reported during runtime can be caused by an expression error in dataset setting and/or activity definition referenced in the pipeline. So it's important to check expressions carefully in _all_ relevant entities <br>

* Please be extra careful when writing JSON within expressions, particularly when using arrays types. For example, if you want to use a JSON array, like [1, 2, 3], as the value of an expression in a ForEach activity, you can write expressions "@json('[1,2,3]')" or "@createArray(1,2,3)", but **not** "@[1,2,3]" <br>
* _Only_ single quotes can be used within expressions, while double quotes are reserved to mark the ends of the entire expression.  Single quotes can be escaped with an additional single quote, however it's may be hard to see depending on font and easy to get wrong. Please use extra caution when leveraging these capabilities.  For example, _one_ in following expression is within pairs of two single quotes (not a pair of double quotes): "@json('{''one'':1}')". <br>
* Consider testing expressions in small pipelines during development, so you can iterate quickly to find and fix expression-level issues before using the expression in a more complex context. Please consider utilize the "Debug" mode in ADF portal experience. See [Iterative Development and Debugging](https://docs.microsoft.com/azure/data-factory/iterative-development-debugging/) <br>


## **Recommended Documents**

Supported by ADF: <br>

* Build dynamic contents with [functions and parameters](https://docs.microsoft.com/azure/data-factory/author-visually#use-functions-and-parameters) <br>
* [Expression Language](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions) <br>
* [System Variables](https://docs.microsoft.com/azure/data-factory/control-flow-system-variables) <br>
* [Functions](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions#functions) including: <br>

  * [String](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions#string-functions) functions only apply to strings <br>
  * [Collection](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions#collection-functions) functions operate over collections, such as arrays, strings, and in some cases dictionaries <br>
  * [Logical](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions#logical-functions) functions are useful inside conditions <br>
  * [Conversion](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions#conversion-functions) functions convert between native types <br>
  * [Math](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions#math-functions) functions are used for either _integer_ or _float_ <br>
  * [Date](https://docs.microsoft.com/azure/data-factory/control-flow-expression-language-functions#date-functions) functions operate over timestamps <br>
