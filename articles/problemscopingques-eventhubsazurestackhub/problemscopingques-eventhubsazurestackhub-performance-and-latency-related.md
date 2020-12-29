<properties
pageTitle="Performance and Latency Related"
description="Performance and Latency Related"
service="microsoft.eventhub"
resource="namespaces"
authors="jfggdl"
ms.author="jafernan"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32689175"
resourceTags=""
productPesIds="16803"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="problemscopingques-eventhubsazurestackhub-performance-and-latency- related"
schemaVersion="1"
ownershipId="AzureMessaging_Common"
/>
# Performance and Latency Related
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Performance and Latency Related",
    "fileAttachmentHint": "",
    "formElements": [
        {
	    "id": "problem_start_time",
	    "order": 1,
	    "controlType": "datetimepicker",
	    "displayLabel": "When did the problem begin?",
	    "required": true
	},
        {
            "id": "problem_azureStackVersion",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Azure Stack build version you are using?",
	    "watermarkText": "Ex) Azure Stack Hub 2005",
            "required": true
        },
        {
            "id": "problem_eventHubsVersion",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the version of the Event Hubs resource provider that you have installed?",
	    "watermarkText": "Ex) Event Hubs 1.2008.0.0",
            "required": false
        },
        {
            "id": "problem_uploadLogs",
            "order": 4,
            "controlType": "radioButtonGroup",
            "displayLabel": "Have you uploaded your logs?",
	    "infoBalloonText": "<a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-log-collection-overview-tzl'>Diagnotics log collection</a>",
            "radioButtonOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                }
	    ],
            "required": false
        },
        {
            "id": "problem_sdkLanguage",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the SDK language and version that you are using.",
            "required": false
        },
	{
	    "id": "problem_description",
	    "order": 6,
	    "controlType": "multilinetextbox",
	    "displayLabel": "Details",
	    "watermarkText": "Provide additional information about your incident.",
	    "required": true,
	    "useAsAdditionalDetails": true
	}
    ],
    "$schema": "SelfHelpContent"
}
---
