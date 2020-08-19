<properties
                pageTitle="Cannot Connect to My Virtual Machine"
                description="Cannot Connect to My Virtual Machine"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32615528"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0023"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Connect to a VM
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "I need guidance with serial console access",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connect_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "last_attempt_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "What was your last attempted time to access the serial console?",
            "required": true
        },
        {
            "id": "machinetype",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What is the operating system of the VM?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Windows 7/Windows 8/Windows 8.1/Windows 10",
                    "text": "Windows 7/Windows 8/Windows 8.1/Windows 10"
                },
                {
                    "value": "Windows Server 2008R2/2012/2012R2/2016/2019",
                    "text": "Windows Server 2008R2/2012/2012R2/2016/2019"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
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
