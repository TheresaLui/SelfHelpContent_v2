<properties 
    pageTitle="I want to get started writing application analytics queries"
    description="I want to get started writing application analytics queries"
    service="microsoft.insights"
    resource="components"
    authors="mcosner"
    ms.author="mcosner"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32402605,32402602"
    productPesIds="15693"
    cloudEnvironments="public, Fairfax, usnat, ussec"
 	articleId="d8446387-6f41-4550-bf36-440a264956a7"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# I want to get started writing application analytics queries

## **Recommended Steps**

The [Kusto Query Language (KQL)](https://blogs.msdn.microsoft.com/ben/2018/10/11/getting-started-with-the-kusto-query-language/) is used by Kusto internally at Microsoft and across a wide portfolio of external services, including Azure Application Insights, Azure Log Analytics, Azure Security Center, and Windows Defender Advanced Threat Protection. For Application Insights components, it's quite common that the default charts need some customization in order to be used for your use case. Alternatively, this allows you to understand the query used to supply the data for a given chart and modify it based on the problem you are trying to solve. Many of the curated experiences through the portal have an "Analytics" button at the top. You can reuse these queries to create Log Search alerts, or consume this data for your own visualizations in Power BI or other tools of your choice. To get started with writing queries against the data you have sent to Application Insights, follow these steps:

1. Start from the overview blade on an Application Insights component, or select a specific chart or control for which you'd like to see the backing query, and click the "Analytics" button to launch the Application Analytics portal
2. Edit the query until you are satisfied with the resulting data set
3. Copy the resulting query into a Log Search alert to run this on a scheduled frequency, or export the query into Power BI or another tool of your choice

Microsoft has partnered with Pluralsight to provide free training that ranges from starting from scratch to advanced topics.

## **Recommended Documents**

* [Kusto Query Language (KQL) Documentation](https://go.microsoft.com/fwlink/?linkid=849499)<br>
* [Pluralsight - Kusto Query Language (KQL) From Scratch](https://www.pluralsight.com/courses/kusto-query-language-kql-from-scratch)
