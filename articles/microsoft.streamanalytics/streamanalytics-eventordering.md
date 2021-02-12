<properties
	pageTitle="Event ordering in Stream Analytics"
	description="Event ordering in Stream Analytics"
	infoBubbleText=""
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="sidramadoss"
	articleId="streamanalytics-eventordering"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32636043"
	resourceTags=""
	productPesIds="15663"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ms.author="sidram"
	ownershipId="AzureData_StreamAnalytics"
/>

# Event ordering in Stream Analytics
Late arrival policy and out of order policy can be configured by selecting 'Event ordering' under Configure on the Azure portal. These settings are applied only when your query has the TIMESTAMP BY clause.

When you are setting up your streaming pipeline, you should account for events that are arriving late or out of order. Consider latency and correctness requirements for your scenario when configuring these settings. Optimizing for data correctness will impact latency and vice versa.

To learn how these settings work and how to configure them, please see these recommended documents.

## **Recommended Documents**

* [What is Event Time and Arrival Time?](https://docs.microsoft.com/azure/stream-analytics/event-ordering#event-time-and-arrival-time)
* [What is late arrival policy?](https://docs.microsoft.com/azure/stream-analytics/event-ordering#what-is-late-arrival-policy)
* [What is out of order policy?](https://docs.microsoft.com/azure/stream-analytics/event-ordering#what-is-out-of-order-policy)
* [What does Adjust or Drop do to incoming events?](https://docs.microsoft.com/azure/stream-analytics/event-ordering#adjust-or-drop-events)
* [Example of these policies in action](https://docs.microsoft.com/azure/stream-analytics/event-ordering#adjust-or-drop-events)
* [Can these settings delay the output of my job?](https://docs.microsoft.com/azure/stream-analytics/event-ordering#can-these-settings-delay-output-of-my-job)
