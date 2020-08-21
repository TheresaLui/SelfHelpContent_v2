<properties
                pageTitle="Migration and Move"
                description="Migration and Move"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32570111,32570112,32570113"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0102"
	ownershipId="Compute_VirtualMachines_Content"
/>
# VM Migration
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Migrate virtual machines to Azure using Azure Site Recovery",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "migration_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "migration_ifvnet",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you migrating the resource in a vNet?",
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
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
