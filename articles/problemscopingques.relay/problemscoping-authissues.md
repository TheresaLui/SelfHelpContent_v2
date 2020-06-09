<properties
pageTitle="Authorization Issues"
description="Authorization Issues"
service="microsoft.relay"
resource="autherrorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32684540"
resourceTags=""
productPesIds="16123"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="relay-issues"
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
            "required": true
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
            "id": "problem_sdkversion",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the SDK and SDK version that you are using ?",
            "required": false
        },
       {
            "id": "problem_token",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Has the token expired for your the operation",
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
