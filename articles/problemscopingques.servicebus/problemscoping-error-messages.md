<properties
pageTitle="Error Messages"
description="Error Messages for various issues like Timeout , Connectivity , Create and delete operations etc."
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633395,32633409,32633400,32633396"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="service-bus-error-msg"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Error Messages realted to Timeout , Connectivity , Create and delete
---
{
    "subscriptionRequired": true,
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
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_ClientInformation",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please specific the client library (.Net, .Net Standard, Java, Python, etc) you are using and the version number?",
            "watermarkText": "Clients used by the application and their version number",
            "required": false,
            "useAsAdditionalDetails": true
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