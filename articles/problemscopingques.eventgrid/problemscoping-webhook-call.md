<properties
pageTitle="Issue calling the webhook "
description="Issue calling the webhook "
service="microsoft.eventgrid"
resource="callwebhook-issues"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32583166"
resourceTags=""
productPesIds="16263"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eg-call-webhook"
schemaVersion="1"
	ownershipId="AzureEventGrid_Topics"
/>
# Issue calling the webhook
---
{
    "subscriptionRequired": true,
    "title": "Issue calling the webhook ",
    "resourceRequired": true,
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
            "id": "problem_endpoint",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Is the webhook an HTTPS endpoint. If not what endpoint are you using",
            "required": true
        },
        {
            "id": "problem_validateendpoint",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you validated the webhook endpoint using the validation event",
            "watermarkText": "Choose an option",
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
                    "value": "i_dont_know",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_cert",
            "order": 4,
             "controlType": "dropdown",
            "displayLabel": "Does your endpoint have a self signed certificate",
            "watermarkText": "Choose an option",
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
                    "value": "i_dont_know",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including call stack, Tracking Id and timestamp, if any",
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
