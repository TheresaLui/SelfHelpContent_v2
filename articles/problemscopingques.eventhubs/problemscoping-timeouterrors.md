<properties
pageTitle="Timeout errors"
description="Timeout errors"
service="microsoft.eventhubs"
resource="timeouterrorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636944"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-timeout-issues"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Timeout errors
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Timeout errors",
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
            "id": "problem_locationofcode",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Are you running the code from Azure or On-premise or external cloud provider?",
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
            "id": "problem_environment",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Does this issue reproduce in multiple environments?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
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
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide the call stack with exception messages and any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
