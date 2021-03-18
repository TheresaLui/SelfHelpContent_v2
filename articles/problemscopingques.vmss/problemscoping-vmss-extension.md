<properties
                pageTitle="Extensions not operating correctly"
                description="Extensions not operating correctly"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32641077, 32641085, 32641086,32641087,32641111,32641115,32641121,32641134,32641154"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0133"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Agent and extensions
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Extensions not operating correctly",
    "fileAttachmentHint": "",
    "diagnosticCard": {
            "title": "Virtual machine scale set diagnostics",
            "description": "These diagnostics will check for details about your selected VM instance within your VMSS.",
            "insightNotAvailableText": "We didn't find any problems"},
    "formElements": [
        {
            "id": "vmss_instance",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "If your issue is related to a specific instance, select the instance name",
            "dynamicDropdownOptions": {
                "uri": "{resourceId}/virtualMachines?api-version=2019-03-01",
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
                    "value": "Unable to retrieve list of instances.",
                    "text": "Unable to retrieve list of instances."
                }
            ],
            "useAsAdditionalDetails": false,
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "extension_error",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
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
