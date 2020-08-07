<properties
                pageTitle="My Virtual Machine restarted, paused, or stopped unexpectedly"
                description="My Virtual Machine restarted, paused, or stopped unexpectedly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628289"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0006"
	ownershipId="Compute_VirtualMachines_Content"
/>
# VM Restart
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Troubleshoot Windows Update issues",
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
            "id": "restart_storage",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What type of Windows Update issue are you having?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Stuck in Windows Update boot screen",
                    "text": "Stuck in Windows Update boot screen"
                },
                {
                    "value": "Windows Update fails to install and retries fail",
                    "text": "Windows Update fails to install and retries fail"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "restart_update",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What Windows Update are you trying to install?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "machinetype",
            "order": 4,
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
            "id": "manageupdate",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "How are you managing Windows Updates?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "GPOs",
                    "text": "GPOs"
                },
                {
                    "value": "SCCM",
                    "text": "SCCM"
                },
                {
                    "value": "Update management Azure portal feature",
                    "text": "Update management Azure portal feature"
                },
                {
                    "value": "Automatic /Manual Windows Update",
                    "text": "Automatic /Manual Windows Update"
                },
                {
                    "value": "Other tool",
                    "text": "Other tool"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
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
