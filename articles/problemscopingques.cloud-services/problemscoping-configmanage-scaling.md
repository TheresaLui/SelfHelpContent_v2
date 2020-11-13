<properties
                pageTitle="Configuration and Management"
                description="Configuration and Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32569897"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0100"
	ownershipId="Compute_CloudServices_Content"
/>
# Config and Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Scaling",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "cloud_service_slots",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Slot",
            "watermarkText": "Choose an option",
            "required": false,
            "dropdownOptions": [{
                "value": "Production",
                "text": "Production"
            }, {
                "value": "Staging",
                "text": "Staging"
            }]
        },
        {
            "id": "cloud_service_roles",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Role",
            "watermarkText": "Choose an option",
            "required": false,
            "visibility": "cloud_service_slots != null && cloud_service_slots != dont_know_answer",
            "dynamicDropdownOptions": {
                "dependsOn": "cloud_service_slots",
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/microsoft.classiccompute/domainnames/{resourceName}/slots/{replaceWithParentValue}/roles?&api-version=2015-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No roles available"
                }
            }
        },
        {
            "id": "scaling_symptom",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the symptom related to your scaling issue?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "autoscale",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "How did you enable AutoScale?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I am using a tool that manages my autoscaling using the Azure rest APIs",
                    "text": "I am using a tool that manages my autoscaling using the Azure rest APIs"
                },
                {
                    "value": "I am using Azure autoscaling through Azure portal",
                    "text": "I am using Azure autoscaling through Azure portal"
                }
            ],
            "required": false
        },
        {
            "id": "autoscale_notification",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "If you have received a notification for AutoScale from Azure, please share.",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
