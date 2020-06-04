<properties
                pageTitle="Virtual Machine Extensions not operating correctly"
                description="Virtual Machines Extensions not operating correctly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32628283"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0050"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Agent and extensions
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "VM Diagnostic (boot diagnostics) extension issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "extension_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "extension_operation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What operation are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Install",
                    "text": "Install"
                },
                {
                    "value": "Uninstall",
                    "text": "Uninstall"
                },
                {
                    "value": "Enable",
                    "text": "Enable"
                },
                {
                    "value": "Troubleshoot",
                    "text": "Troubleshoot"
                },
                {
                    "value": "I do not know",
                    "text": "I do not know"
                }
            ],
            "required": false
        },
        {
            "id": "extension_installed",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the extension installed?",
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
            "id": "extension_agentinstalled",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Do you have the latest Azure VM Agent installed?",
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
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
