<properties
pageTitle="Errors and Issues"
description="Errors and Issues"
service="microsoft.relay"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32684541,32684547,32684542,32684543"
resourceTags=""
productPesIds="16123"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="relay-error-msg"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Errors and Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired":true,
    "title": "Error messages",
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
            "required": false
        },
       {
            "id": "problem_firewall",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Do you have a firewall or proxy in place on your client environment",
            "required": false
          },
        {
            "id": "problem_ClientInformation",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please specific the SDK client library you are using and the version number?",
            "watermarkText": "Clients used by the application and their version number",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
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