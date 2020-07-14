<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32583111"
                productPesIds="14749,15571,15797,16454,16470"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0089"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Instance Metadata Service",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "manage_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "manage_operation",
            "order": 2,
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
