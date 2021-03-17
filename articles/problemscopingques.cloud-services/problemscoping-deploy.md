<properties
                pageTitle="Deployment"
                description="Deployment"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32565474,32565476,32565478,32565479,32591243"
                productPesIds="13185"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0101"
	ownershipId="Compute_CloudServices_Content"
/>
# Deployment
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
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
            "id": "failure_frequency",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the frequency of deployment failure?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Every deployment",
                    "text": "Every deployment"
                },
                {
                    "value": "Fails on multiple retries",
                    "text": "Fails on multiple retries"
                },
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
                }
            ],
            "required": false
        },
        {
            "id": "if_fromportal",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Does this issue occur when deploying from the portal?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "Have not tried it",
                    "text": "Have not tried it"
                },
                {
                    "value": "Happens only from client tools (VS, PS)",
                    "text": "Happens only from client tools (VS, PS)"
                }
            ],
            "required": false
        },
        {
            "id": "deploy_error",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message (include Operation ID etc).",
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
