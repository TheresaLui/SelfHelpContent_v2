<properties
pageTitle="Questions on Kafka Configuration"
description="Questions on Kafka Configuration"
service="microsoft.eventhubs"
resource="khafkaconfiguration"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636949,32742759,32742760,32742761"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-khafka-config"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Questions on Kafka Configuration
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Questions on Kafka Configuration",
    "fileAttachmentHint": "For faster resolution please upload the Kafka config details",
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
                "valuePropertyRegex": "^+$",
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
            "id": "problem_khafkaversion",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Which Kafka client library are you using and what version?",
            "required": true
        },
        {
            "id": "getKafkaConfigFile",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you checked your Kafka configuration conforms to our recommendations?",
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
                    "value": "dont_know_answer",
                    "text": "I didn't check"
                }
            ],
            "infoBalloonText": "You can avoid common issues with Kafka by following the <a href='https://github.com/Azure/azure-event-hubs-for-kafka/blob/master/CONFIGURATION.md'>recommended configuration settings</a>.",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your issue here",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---