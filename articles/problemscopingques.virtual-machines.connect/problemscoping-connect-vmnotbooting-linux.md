<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615532"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0031"
	ownershipId="Compute_VirtualMachines"
/>
# Connect to a VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My VM is not booting",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connect_request",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What do you need help with?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Recover my VM from a boot failure",
                    "text": "Recover my VM from a boot failure"
                },
                {
                    "value": "Recreate the Virtual Machine",
                    "text": "Recreate the Virtual Machine"
                },
                {
                    "value": "Root cause analysis",
                    "text": "Root cause analysis"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
