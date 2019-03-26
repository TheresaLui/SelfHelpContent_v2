<properties
                pageTitle="Cannot Deploy a Virtual Machine"
                description="Cannot Deploy a Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628259"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0034"
/>
# Deploy a VM
---
{
    "resourceRequired": true,
    "title": "I am unable to deploy a captured or generalized image",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "resourceGroup",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select resource group for deployment failure",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourcegroups?api-version=2018-05-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of resource groups.",
                    "text": "Unable to retrieve list of resource groups."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "correlationId",
            "order": 2,
            "visibility": "resourceGroup != null",
            "controlType": "dropdown",
            "displayLabel": "Select failed deployment",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "/subscriptions/{subscriptionId}/resourcegroups/{resourceGroup}/providers/Microsoft.Resources/deployments/?api-version=2018-05-01&$filter=provisioningState%20eq%20'Failed'&$top=10",
                "jTokenPath": "value",
                "textProperty": "properties.timestamp,properties.parameters.location.value,name",
                "textTemplate": "Time:{properties.timestamp} Region:{properties.parameters.location.value} Name:{name}",
                "valueProperty": "properties.correlationId",
                "defaultDropdownOptions": {
                    "value": "Deployment failure not found.",
                    "text": "Deployment failure not found."
                },
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of failed deployments.",
                    "text": "Unable to retrieve list of failed deployments."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "deployment_from",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What are you trying to create your VM from?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "VHD file",
                    "text": "VHD file"
                },
                {
                    "value": "Snapshot",
                    "text": "Snapshot"
                },
                {
                    "value": "Captured image",
                    "text": "Captured image"
                },
                {
                    "value": "Backup",
                    "text": "Backup"
                }
            ],
            "required": false
        },
        {
            "id": "problem_snapshot_date",
            "order": 4,
            "visibility": "deployment_from == Snapshot",
            "controlType": "datetimepicker",
            "displayLabel": "When was the time of the attempted snapshot?",
            "required": true
        },
        {
            "id": "problem_caputre_date",
            "order": 5,
            "visibility": "deployment_from == Captured image",
            "controlType": "datetimepicker",
            "displayLabel": "When was the time of the image capture?",
            "required": true
        },
        {
            "id": "problem_restore_date",
            "order": 6,
            "visibility": "deployment_from == Backup",
            "controlType": "datetimepicker",
            "displayLabel": "When was the time of the attempted backup?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ]
}
---
