<properties
                pageTitle="My Virtual Machine restarted, paused, or stopped unexpectedly"
                description="My Virtual Machine restarted, paused, or stopped unexpectedly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628287"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0001"
	ownershipId="Compute_VirtualMachines_Content"
/>
# VM Restart
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Help diagnose my VM restart issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "restart_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
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
            "useAsAdditionalDetails": false,
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
