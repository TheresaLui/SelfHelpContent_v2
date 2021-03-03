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
articleId="sb-dead-letter-errors-resource"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Unexpected Message Dead Lettering
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unexpected Message Dead Lettering",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "servicebus_feature",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Service Bus feature",
            "watermarkText": "Choose an option",
            "required": false,
            "dropdownOptions": [{
                "value": "Queues",
                "text": "Queues"
            }, {
                "value": "Topics",
                "text": "Topics"
            }]
        },
        {
            "id": "servicebus_queues",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Queue names",
            "watermarkText": "Choose an option",
            "required": false,
            "visibility": "servicebus_feature != null && servicebus_feature == Queues",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.ServiceBus/namespaces/{resourceName}/queues?&api-version=2015-08-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No queues available"
                }
            }
        },
        {
            "id": "servicebus_topics",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Topic names",
            "watermarkText": "Choose an option",
            "required": false,
            "visibility": "servicebus_feature != null && servicebus_feature == Topics",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.ServiceBus/namespaces/{resourceName}/topics?&api-version=2015-08-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No topics available"
                }
            }
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_issueFrequency",
            "order": 5,
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
            "order": 6,
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