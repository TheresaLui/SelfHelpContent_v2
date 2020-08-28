<properties
pageTitle="Issues with Install, Uninstall, or Update"
description="Issues with Install, Uninstall, or Update"
service="microsoft.eventhub"
resource="namespaces"
authors="jafernan"
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
	    "watermarkText": "Ex) Event Hubs 1.2008.0.0", 
            "required": false
        },
        {
            "id": "problem_errorMessageText",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id, and timestamp, if any.",
            "required": false
        },
        {
            "id": "problem_errorFrequency",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the frequency of the error(s)?",
            "required": false
        },
        {
            "id": "problem_uploadLogs",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Have you initiated the upload of logs following the steps in [Diagnotics log collection](https://docs.microsoft.com/azure-stack/operator/azure-stack-diagnostic-log-collection-overview-tzl)?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
