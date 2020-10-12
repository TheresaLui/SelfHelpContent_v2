<properties
	pageTitle="Common Solutions Template"
	description="Common Solutions Template"
	infoBubbleText="Common Solutions Template"
	service=""
	resource=""
	ms.author=""
	displayOrder=""
	articleId=""
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments=""
	ownershipId=""
/>

# <-- This is the title of the article. It is not displayed in the portal, however, an **H1** header is a required part of every article. -->

This is a brief paragraph about the problem. It can be as simple as "Most users are able to resolve their [topic] issue using the steps below", or a more detailed outline of the issue being experienced.

## **Recommended Steps**

1. This is a step with a link to an [external article](https://)
2. This is a step with no link, blade, or instructions. Note that because the next line is a continuation of the list, no <br> (br) break is needed.
3. As in the example above, this step contains multiple sentences. When a step has multiple complete sentences, the use of a period to end each sentence is acceptable.
4. This step does not have multiple sentences, so no period is required at the end
5. This is a step with a [link to a blade](data-blade:extensionName.bladeName.nameOfInputParam.valueOfInputParam)
6. This is a step with a single line or snippet of code: `SELECT name, is_disabled FROM sys.sql_logins`
7. This is a step with multi-line code:

```
[cluster my-cluster]
    FormLayout = selectionpanel
    Category = My Templates
    CategoryOrder = 100
    MaxCount = 200
    Autoscale = $Autoscale
```

Below is an example of a bulleted list. Note that only 2 levels of bullets are supported:

* Item1
* Item2
* Item3
	* Sub-ItemA
	* Sub-ItemB

All lists require an empty line before the first item and after the last item.

## **Recommended Documents**

* [This is the display text of an external document](https://)
* [This is the display text for the last article in the list](http://)

### Notes

* The **Recommended Steps** and **Recommended Documents** headings must be entered as shown above (bolded H2)
* Formatting is not identical to Microsoft Docs - tables do not work, nor [!NOTE] tags
* Your Recommended Steps should be actual steps, not just links to other articles
* Ensure all links to Microsoft docs are non-region-specific, i.e. does not include /en-us/. This does not apply to articles for Mooncake.
* Don't link to internal review documentation - these URLs always start with "review.microsoft.docs", and users are unable to access them
* Do not use aka.ms links
* Copy the raw form of this article to use as a template for your own Common Solution article. Be sure to fill in the metadata!
