<properties
                pageTitle="My Virtual Machine restarted, paused, or stopped unexpectedly"
                description="My Virtual Machine restarted, paused, or stopped unexpectedly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628269"
                productPesIds="15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0002"
	ownershipId="Compute_VirtualMachines"
/>
# VM Restart
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My guest OS is causing restarts",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "restart_storage",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Are your VMs using Standard Storage or Premium Storage?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Standard Storage",
                    "text": "Standard Storage"
                },
                {
                    "value": "Premium Storage",
                    "text": "Premium Storage"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "machinetype",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which machine version are you running?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Ubuntu",
                    "text": "Ubuntu"
                },
                {
                    "value": "Redhat",
                    "text": "Redhat"
                },
                {
                    "value": "Other",
                    "text": "Other"
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
