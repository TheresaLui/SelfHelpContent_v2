<properties
pageTitle="Request to scale up dedicated Sku"
description="Request to dedicated Sku"
service="microsoft.eventhubs"
resource="scaleupdedicatedcluster"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636957"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-scale-dedicated-sku-request"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Request to scale up Event Hubs Dedicated Sku
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Request to scale up Event Hubs Dedicated Sku",
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
            "id": "problem_capacityUnits",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "How many capacity units are your requesting for?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "1",
                    "text": "1"
                },
                 {
                    "value": "2",
                    "text": "2"
                },
                 {
                    "value": "4",
                    "text": "4"
                },
                {
                    "value": "8",
                    "text": "8"
                },
                 {
                    "value": "12",
                    "text": "12"
                },
                 {
                    "value": "16",
                    "text": "16"
                },
                 {
                    "value": "20",
                    "text": "20"
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