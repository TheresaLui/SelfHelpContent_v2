<properties
                pageTitle="My VM is not booting"
                description="My VM is not booting"
                authors="timbasham"
                ms.author="tibasham"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32675597"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="938c78d3-4209-4536-a91a-c1398c28f755"
	ownershipId="Compute_VirtualMachines_Content"
/>
# My VM is not booting
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "My VM is not booting",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "notbooting_whatupate",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What update was applied?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "notbooting_rcaonly",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Root cause analysis only (no mitigation needed)?",
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
            "id": "notbooting_providevhd",
            "order": 3,
            "visibility": "notbooting_rcaonly == Yes",
            "controlType": "dropdown",
            "displayLabel": "Are you willing to provide the VHD of the VM for the investigation?",
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
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ]
}
---
