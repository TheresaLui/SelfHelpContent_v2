<properties
                pageTitle="My VM is not booting"
                description="My VM is not booting"
                authors="timbasham"
                ms.author="tibasham"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32675599"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="35274616-00b8-4efa-820a-1aa6c988c960"
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
            "id": "notbooting_priorchange",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What was the most recent change to the VM?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Updates were applied",
                    "text": "Updates were applied"
                },
                {
                    "value": "Software was installed",
                    "text": "Software was installed"
                },
                {
                    "value": "A role or feature was added or removed",
                    "text": "A role or feature was added or removed"
                },
                {
                    "value": "Updates were made to a group policy",
                    "text": "Updates were made to a group policy"
                },
                {
                    "value": "Unknown",
                    "text": "Unknown"
                }
            ],
            "required": false
        },
        {
            "id": "notbooting_softwareinstalled",
            "order": 2,
            "visibility": "notbooting_priorchange == Software was installed",
            "controlType": "dropdown",
            "displayLabel": "What type of software was installed?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Anti-virus",
                    "text": "Anti-virus"
                },
                {
                    "value": "Firewall",
                    "text": "Firewall"
                },
                {
                    "value": "Citrix",
                    "text": "Citrix"
                },
                {
                    "value": "VPN client",
                    "text": "VPN client"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "notbooting_whatupate",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What update was applied?",
            "useAsAdditionalDetails": false,
            "required": false
        },
        {
            "id": "notbooting_rcaonly",
            "order": 4,
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
            "order": 5,
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
    ]
}
---
