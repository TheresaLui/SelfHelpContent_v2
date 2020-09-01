<properties
pageTitle="Unexpected Service Behavior"
description="Unexpected Message Dead Lettering"
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633410"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-dead-letter-errors"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Unexpected Message Dead Lettering
---
{
    "subscriptionRequired": true,
    "title": "Unexpected Message Dead Lettering",
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
            "id": "problem_deadletterreason",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the DeadLetterReason value",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "HeaderSizeExceeded",
                    "text": "The size quota for this stream has been exceeded."
                },
                {
                    "value": "TTLExpiredException",
                    "text": "The message expired and was dead lettered."
                },
                {
                    "value": "NullSessionID",
                    "text": "Session enabled entity doesn't allow a message whose session identifier is null."
                },
                {
                    "value": "MaxTransferHopCountExceeded",
                    "text": "Maximum Transfer Hop count has exceeded"
                },
                {
                    "value": "Application Specific Value or empty",
                    "text": "Application Specific Value or empty"
                },
                {
                    "value": "Filtering Specific Failure Exception",
                    "text": "Filtering Specific Failure Exception"
                },
                {
                    "value": "MessageDeliveryCountExceeded",
                    "text": "Message could not be consumed after 'n' delivery attempts."
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 4,
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