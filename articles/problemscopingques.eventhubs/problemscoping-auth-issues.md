<properties
pageTitle="Authorization Issues"
description="Authorization Issues"
service="microsoft.eventhubs"
resource="autherrorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636945"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-auth-issues"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Authorization Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Authorization Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "eventhubs_namespaces",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Event Hubs",
            "watermarkText": "Choose an option",
            "required": false,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.EventHub/namespaces/{resourceName}/eventhubs?&api-version=2015-08-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No event hubs available"
                }
            }
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_issueFrequency",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How frequently does the issue occur?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Always",
                    "text": "Always"
                },
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
                },
                {
                    "value": "DontKnow",
                    "text": "Didn't notice any trend"
                }
            ]
        },
        {
            "id": "problem_errorMessageText",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
            "required": true
        },
        {
            "id": "problem_permissions",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "What permissions does your key have to perform the operation?",
            "required": true,
            "watermarkText": "Choose one or more permissions used by your key",
            "dropdownOptions": [
                {
                    "value": "Send",
                    "text": "Send"
                },
                {
                    "value": "Listen",
                    "text": "Listen"
                },
                {
                    "value": "Manage",
                    "text": "Manage"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
         {
            "id": "problem_sdkversion",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the SDK and SDK version that you are using ?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
