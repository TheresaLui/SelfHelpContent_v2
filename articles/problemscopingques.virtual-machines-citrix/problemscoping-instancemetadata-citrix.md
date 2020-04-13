<properties
                pageTitle="Management"
                description="Management"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32587973"
                productPesIds="16215"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0112"
	ownershipId="Compute_VirtualMachines"
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
            "id": "citrixcase",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Do you have a support case with Citrix?",
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
            "id": "citrixcase_id",
            "order": 2,
            "visibility": "citrixcase == Yes",
            "controlType": "textbox",
            "displayLabel": "Citrix support case number",
            "required": true
        },
        {
            "id": "manage_error",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false,
            "useAsAdditionalDetails": true
        },
        {
            "id": "manage_operation",
            "order": 4,
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
