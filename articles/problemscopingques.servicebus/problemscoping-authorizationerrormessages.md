<properties
pageTitle="Authorization Issues"
description="Authorization Issues"
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633394"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-auth-issues"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Authorization Issues
---
{
    "subscriptionRequired": true,
    "title": "Authorization Issues",
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
            "id": "problem_issueFrequency",
            "order": 2,
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
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_permissions",
            "order": 4,
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": false,
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