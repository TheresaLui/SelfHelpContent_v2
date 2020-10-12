<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32583111"
                productPesIds="16080"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0107"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Instance Metadata Service",
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
            "id": "manage_error",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "manage_operation",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "What operation are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Tracking VM running on Azure",
                    "text": "Tracking VM running on Azure"
                },
                {
                    "value": "Placement of containers, data-partitions based fault/update domain",
                    "text": "Placement of containers, data-partitions based fault/update domain"
                },
                {
                    "value": "Getting more information about the VM during support case",
                    "text": "Getting more information about the VM during support case"
                },
                {
                    "value": "Getting Azure Environment where the VM is running",
                    "text": "Getting Azure Environment where the VM is running"
                },
                {
                    "value": "Validating that the VM is running in Azure",
                    "text": "Validating that the VM is running in Azure"
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
