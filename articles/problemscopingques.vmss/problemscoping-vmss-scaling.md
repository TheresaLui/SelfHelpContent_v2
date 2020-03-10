<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32641082"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0201"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Scaling issue with my scale set",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "scaling_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you are getting?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "problem_last_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When was the last time the issue occurred?",
            "required": true
        },
        {
            "id": "scaling_metrics",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What metrics are you using?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "scaling_if_worked",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you ever successfully scaled your VMSS?",
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
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
