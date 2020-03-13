<properties
                pageTitle="VM Guest Agent issue (crash, hung, not upgrading, or not connecting)"
                description="VM Guest Agent issue (crash, hung, not upgrading, or not connecting)"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32689203"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax"
                schemaVersion="1"
                articleId="299e5964-a726-47f3-9722-829ffb6d360f"
	ownershipId="Compute_VirtualMachines_Content"
/>
# VM Guest Agent issue (crash, hung, not upgrading, or not connecting)
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "My issue or extension isn’t listed above",
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
            "id": "vm_extension",
            "order": 2,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select all the applicable extensions you are having issue with",
            "dynamicDropdownOptions": {
                "uri": "{resourceId}/extensions?api-version=2019-03-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of extensions.",
                    "text": "Unable to retrieve list of extensions."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "extension_configure",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What extension are you trying to configure?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "extension_operation",
            "order": 4,
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
            "id": "extension_agentinstalled",
            "order": 5,
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
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
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
