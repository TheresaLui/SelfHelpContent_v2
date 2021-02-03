<properties
pageTitle="Issues with Install, Uninstall, or Update"
description="Issues with Install, Uninstall, or Update"
service="microsoft.eventhub"
resource="namespaces"
authors="jfggdl"
ms.author="jafernan"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32689173"
resourceTags=""
productPesIds="16803"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="problemscopingques-eventhubsazurestackhub-install-uninstall-update"
schemaVersion="1"
ownershipId="AzureMessaging_Common"
/>
# Issues with Install, Uninstall, or Update
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues with Install, Uninstall, or Update",
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
            "id": "problem_errorMessageText",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id, and timestamp, if any.",
            "required": false
        },
        {
            "id": "problem_errorFrequency",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the frequency of the error(s)?",
            "required": false
        },
        {
            "id": "problem_uploadLogs",
            "order": 6,
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
	    "id": "problem_description",
	    "order": 7,
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
