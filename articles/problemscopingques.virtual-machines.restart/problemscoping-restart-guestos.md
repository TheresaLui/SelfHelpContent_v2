<properties
                pageTitle="My Virtual Machine restarted, paused, or stopped unexpectedly"
                description="My Virtual Machine restarted, paused, or stopped unexpectedly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628269"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0003"
	ownershipId="Compute_VirtualMachines_Content"
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
                    "value": "Windows 7/Windows server 2008r2",
                    "text": "Windows 7/Windows server 2008r2"
                },
                {
                    "value": "Windows 8/Windows server 2012",
                    "text": "Windows 8/Windows server 2012"
                },
                {
                    "value": "Windows 8.1/Windows server 2012r2",
                    "text": "Windows 8.1/Windows server 2012r2"
                },
                {
                    "value": "Windows 10/Windows server 2016",
                    "text": "Windows 10/Windows server 2016"
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
