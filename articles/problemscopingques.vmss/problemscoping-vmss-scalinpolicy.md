<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32688664"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0200"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Scaling issue when using scale-in policy",
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
            "id": "scaling_if_deletion",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the issue the deletion of a wrong instance?",
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
            "id": "scaling_instance_number",
            "order": 3,
            "visibility": "scaling_if_deletion == Yes",
            "controlType": "textbox",
            "displayLabel": "What were the instance numbers that were scaled in?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "scaling_scalein",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you able to configure the VMSS to use Scale In Policy?",
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
