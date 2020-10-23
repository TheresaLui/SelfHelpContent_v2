<properties
pageTitle="Request for dedicated Sku"
description="Request for dedicated Sku"
service="microsoft.eventhubs"
resource="dedicatedclusterRequest"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32636954"
resourceTags=""
productPesIds="16125"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="eh-dedicated-sku-request"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Request for Event Hubs Dedicated Sku
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Request for Event Hubs Dedicated Sku",
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
            "id": "problem_capacityUnits",
            "order": 2,
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
            "id": "problem_clustername",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is your preferred cluster name?",
            "watermarkText": "Please enter a unique name for your cluster",
            "required": false
        },
        {
            "id": "problem_region",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What region do you want to create the cluster in?",
            "watermarkText": "Please enter the region where the cluster needs to be created",
            "required": false
        },
        {
            "id": "problem_subcription",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Which subscription ID  would you like to provision your cluster to belong to?",
            "watermarkText": "Provide Subscription ID",
            "required": false
        },
       {
            "id": "problem_resourcegroup",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Which the resource group would you like to provision your cluster in?",
            "watermarkText": "Provide resource group name",
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