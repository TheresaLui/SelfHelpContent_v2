<properties
	  pageTitle="Generated time shown in the WS is different from the real creation time"
	  description="Generated time shown in the WS is different from the real creation time"
      service="Microsoft.Security"
      resource="Microsoft.Security/alerts"
	  authors="rimayber"
	  ms.author="rimayber"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="58e98a42-b14e-4871-ad4c-d21cd274d566"
	  ownershipId="Azure_Sentinel"
/>

# Generated time shown in the WS is different from the real creation time

By default, the Log Analytics agent populates the TimeGenerated field in the schema with the time the agent received the event from the Syslog daemon. As a result, the time at which the event was generated on the source system is not recorded in Azure Sentinel. In order to populate the TimeGenerated field with the event's original time on its source system, please follow steps [described in this doc](https://docs.microsoft.comazure/sentinel/connect-cef-agent?tabs=rsyslog)

