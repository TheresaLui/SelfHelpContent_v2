<properties
                pageTitle="Cannot Start or Stop My Virtual Machine"
                description="Cannot Start or Stop My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628282"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0010"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Start or Stop My VM
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My start or stop operation failed",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "startstop_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "startstop_operation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you trying to start or stop your VM?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Start",
                    "text": "Start"
                },
                {
                    "value": "Stop",
                    "text": "Stop"
                }
            ],
            "required": false
        },
        {
            "id": "startstop_othervm",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Do you have trouble starting/stopping any of the other VMs under the same cloud service?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
