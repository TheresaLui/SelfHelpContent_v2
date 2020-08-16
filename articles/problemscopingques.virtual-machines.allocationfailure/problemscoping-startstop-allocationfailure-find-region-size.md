<properties
pageTitle="Recieved an Allocation Failure"
description="Recieved an Allocation Failure"
authors="summertgu"
ms.author="tiag"
selfHelpType="problemScopingQuestions"
supportTopicIds="32743100"
productPesIds="14749,15571,15797,16454,16470"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
articleId="6dd1f126-a89d-497e-9a83-eb4a21e33091"
ownershipId="Compute_VirtualMachines_Content"
/>
# Recieved an Allocation Failure

---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Need help finding a new region or size",
    "fileAttachmentHint": "",
    "diagnosticCard": {
            "title": "Virtual machine deployment diagnostics",
            "description": "These diagnostics will check for details about your selected deployment failure.",
            "insightNotAvailableText": "We didn't find any problems"},
    "formElements": [
    {
        "id": "allocation_region",
        "order": 1,
        "controlType": "dropdown",
        "watermarkText": "Choose an option",
        "displayLabel": "What region/location are you deploying to?",
        "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "name",
            "textPropertyRegex": "[^/]+$",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            }
        },
        "dropdownOptions": [
        {
            "value": "Unable to retrieve list of regions.",
            "text": "Unable to retrieve list of regions."
        }
        ],
            "useAsAdditionalDetails": false,
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
    },
    {
        "id": "allocation_size",
        "order": 2,
        "visibility": "allocation_region != null && allocation_region != dont_know_answer",
        "controlType": "dropdown",
        "watermarkText": "Choose an option",
        "displayLabel": "What VM size are you trying to deploy?",
        "dynamicDropdownOptions": {
            "dependsOn": "allocation_region",
            "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Compute/locations/{replaceWithParentValue}/vmSizes?api-version=2019-07-01",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "name",
            "textPropertyRegex": "[^/]+$",
            "valuePropertyRegex": "[^/]+$",
            "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            }
        },
        "dropdownOptions": [
        {
            "value": "Unable to retrieve list of VM sizes.",
            "text": "Unable to retrieve list of VM sizes."
        }
        ],
            "useAsAdditionalDetails": false,
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
    },
    {
        "id": "allocation_count",
        "order": 3,
        "controlType": "textbox",
        "displayLabel": "How many instances are you deploying?",
        "required": true,
        "useAsAdditionalDetails": false,
        "diagnosticInputRequiredClients": "Portal,ASC"
    },
    {
            "id": "startstop_operation",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What operation are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create",
                    "text": "Create"
                },
                {
                    "value": "Start",
                    "text": "Start"
                },
                {
                    "value": "Resize",
                    "text": "Resize"
                },
                {
                    "value": "Redeploy",
                    "text": "Redeploy"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_isinavailabilitysetzone",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying your VM in an availability set or zone?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_isinscaleset",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Are you deploying your VM in a scale set?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "correlation_id",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Correlation ID",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
