<properties
pageTitle="Monitoring and Diagnostics"
description="Monitoring and Diagnostics"
service="microsoft.eventhub"
resource="namespaces"
authors="jfggdl"
ms.author="jafernan"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32689174"
resourceTags=""
productPesIds="16803"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="problemscopingques-eventhubsazurestackhub-monitoring-and-diagnostics"
schemaVersion="1"
ownershipId="AzureMessaging_Common"
/>
# Monitoring and Diagnostics
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Monitoring and Diagnostics",
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
	    "id": "problem_description",
	    "order": 4,
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
