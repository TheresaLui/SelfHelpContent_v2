<properties
pageTitle="Performance and Latency Related"
description="Performance and Latency Related"
service="microsoft.eventhub"
resource="namespaces"
authors="jafernan"
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
            "id": "problem_azureStackVersion",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Azure Stack build version you are using?",
	    "watermarkText": "Ex) Azure Stack Hub 2005",
            "required": true
        },
        {
            "id": "problem_eventHubsVersion",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the version of the Event Hubs resource provider that you have installed?",
            "required": false
        },    
        {
            "id": "problem_uploadLogs",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Have you initiated the upload of logs following the steps in Diagnotics log collection? https://docs.microsoft.com/en-us/azure-stack/operator/azure-stack-diagnostic-log-collection-overview-tzl?",
            "required": false
        },
        {
            "id": "problem_sdkLanguage",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the SDK language and version that you are using.",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
