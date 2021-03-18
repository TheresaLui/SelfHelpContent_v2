<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32641082,32641116,32641131,32641132,32641133,32641142"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0201"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Scaling issue with my scale set",
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
            "id": "scaling_error",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you are getting?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "problem_last_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When was the last time the issue occurred?",
            "required": true
        },
        {
            "id": "scaling_metrics",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What metrics are you using?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "scaling_if_worked",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Have you ever successfully scaled your VMSS?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
