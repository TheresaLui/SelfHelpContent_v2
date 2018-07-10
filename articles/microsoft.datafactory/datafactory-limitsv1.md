<properties 
	pageTitle="Data factory limits" 
	description="I got an error about exceeding a data factory limit" 
	service="microsoft.datafactory" 
    resource="datafactories"
    authors="arthurw"
    displayOrder="10"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds="32356640,32356646,32356648,32356669"
    productPesIds="15613"
    resourceTags=""
/>

# Data Factory Limits

## **Recommended steps**
- Default limits are often increased based on patterns of customer requests, and some limits (including bytes per object for pipeline objects)
can not be increased above the default, so please check the documentation linked below for current information before requesting a limit increase.<br/>
- If you hit the bytes per object for pipeline objects limit, the recommended approach is to split the pipeline into several smaller pipelines.<br/>

## **Recommended documents**
[Data Factory Limits (see the Version 1 section)](https://docs.microsoft.com/azure/azure-subscription-service-limits#data-factory-limits)
