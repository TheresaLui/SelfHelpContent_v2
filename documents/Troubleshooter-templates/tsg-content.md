<properties
	pageTitle="Enter the page title"
	description="Brief description of the article"
	service="service provider"
	resource="resource type"
	ms.author="Your Microsoft alias"
	selfHelpType="TSG_Content"
	cloudEnvironments="public, fairfax, ussec, usnat, mooncake"
	articleId="Unique field - use article name OR [a generated GUID](https://www.guidgenerator.com/online-guid-generator.aspx)"
	ownershipId="this is required"
/>

# <Title for the article. This text is presented at the top of the card>

This is a brief paragraph about the problem or the steps you are asking the user to take.

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

Below is an example of a bulleted list. Note that only **2 levels** of bullets are supported:

* Item1
* Item2
* Item3
	* Sub-ItemA
	* Sub-ItemB

All lists require an empty line before the first item and after the last item.

### **H3 Header**

Bolded H2 headers are reserved for **Recommended Steps** or **Recommended Documents**. If you wish to use a header to separate sections, use the H3 header. Double asterisks on either side of the header (after the ###) will bold the text.

## **Recommended Documents**

* [This is the display text of an external document](https://)
* [This is the display text for the last article in the list](http://)

### Notes

* In the metadata, **selfHelpType="TSG_Content"** does not need to be changed
* The Cloud Environments metadata property lists all available environments. Delete the ones not needed from the list: **cloudEnvironments="public, fairfax, ussec, usnat, mooncake"**
* The **Recommended Steps** and **Recommended Documents** headings must be entered as shown above (bolded H2)
* Formatting is not identical to Microsoft Docs - tables do not work, nor [!NOTE] tags
* Your Recommended Steps should be actual steps, not just links to other articles
* Ensure all links to Microsoft docs are non-region-specific, i.e. does not include /en-us/. This does not apply to articles for Mooncake.
* Don't link to internal review documentation - these URLs always start with "review.microsoft.docs", and users are unable to access them
* Do not use aka.ms links
* Copy the raw form of this article to use as a template for your own Common Solution article. Be sure to fill in the metadata!

