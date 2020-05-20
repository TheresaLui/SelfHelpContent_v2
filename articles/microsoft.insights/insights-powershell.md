<properties 
    pageTitle="I need help using powershell to automate my Application Insights deployments"
    description="General troubleshooting guide for ARM deployment"
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    ms.author="jamdavi"
    articleId="insights-powershell"
    displayOrder="97"
    selfHelpType="generic"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    productPesIds="15693" 
    supportTopicIds="32602216,32632995"
 	ownershipId="AzureMonitoring_ApplicationInsights"
/>
 
# I need help using powershell to automate my Application Insights deployments

Most of our cmdlets work by calling an ARM endpoint and should work so long as you have access to the resource or the subscription. Below are the most common questions we get with PowerShell and Application Insights.<br>

**How can I automate with operations on Application Insights resources with PowerShell?**

Application Insights has a variety of PowerShell cmdlets that help automate common interactions with the service:

* To create a new resource use **New-AzureRmApplicationInsights** or **Remove-AzureRmApplicationInsights** to delete one 
* To manage your Application Insights resource’s daily cap using **Get-AzureRmApplicationInsights -IncludeDailyCap** to retrieve the current value, or **Set-AzureRmApplicationInsightsDailyCap** to set a new cap
* To manage your Application Insights resource’s Continuous Export rules, use **Get-AzureRmApplicationInsightsContinuousExport**, **Set-AzureRmApplicationInsightsContinuousExport**, **New-AzureRmApplicationInsightsContinuousExport**, and **Remove-AzureRmApplicationInsightsContinuousExport**
* To manage your Application Insights resource’s API keys using **Get-AzureRmApplicationInsightsApiKey**, **New-AzureRmApplicationInsightsApiKey**, and **Remove-AzureRmApplicationInsightsApiKey**

**How to work with Application Insights resources using an ARM template?**<br>

1. Review the [Deploy resources with templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-template-deploy) guide.
2. Review the [Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/powershell#create-an-azure-resource-manager-template) ARM template doc

**How do I troubleshoot issues using the Application Insights ARM template?**

If you’re getting an error using the Application Insights ARM template, [this page](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors) will guide you through steps to understand and mitigate the error. 

## **Recommended Documents**

* [Deploy resources with templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-template-deploy)
* [Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/powershell#create-an-azure-resource-manager-template)
* [Deployment Errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)
