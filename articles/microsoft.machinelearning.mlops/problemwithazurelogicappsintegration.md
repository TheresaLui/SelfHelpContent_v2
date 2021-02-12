<properties
	pageTitle="Problem with Azure Logic Apps integration"
	description="Problem with Azure Logic Apps integration"
	infoBubbleText="Problem with Azure Logic Apps integration"
	service="microsoft.machinelearning"
	resource="runs"
	authors="mx-iao"
	ms.author="minxia"
	supportTopicIds="32755210"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.runs.problemwithazurelogicappsintegration"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem with Azure Logic Apps integration

## **Recommended Steps**

Azure Machine Learning events are published through [Azure Event Grid](https://docs.microsoft.com/azure/machine-learning/how-to-use-event-grid). You can configure [Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps/logic-apps-overview) to handle the events.

Examples:
* [Use Azure Logic Apps to configure emails for your events](https://docs.microsoft.com/azure/machine-learning/how-to-use-event-grid#example-send-email-alerts)
* [Use Azure Logic Apps to trigger retraining when data drift is detected](https://docs.microsoft.com/azure/machine-learning/how-to-use-event-grid#example-data-drift-triggers-retraining)
