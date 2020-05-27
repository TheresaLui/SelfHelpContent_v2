<properties
            pageTitle="Scoping questions for Site Recovery (Hyper-V to Azure)/Unable to connect"
            description="Cannot Connect to My Hyper-V VM after failover"
            authors="genlin"
            ms.author="asgang"
            selfHelpType="problemScopingQuestions"
            supportTopicIds="32536423"
            productPesIds="16370"
            cloudEnvironments="Public, Fairfax, usnat, ussec"
            schemaVersion="1"
            articleId="e59636d3-914b-40ee-9abd-95bac066ae4e"
	ownershipId="Compute_SiteRecovery"
/>
# Connect to a Hyper-V VM after failover
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Failure to connect to the RDP port",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connect_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message that you received?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "vm_facing_issue",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which virtual machines are experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": true
        },
        {
            "id": "ippublicprivate",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Does the problem occur when you try to connect to the virtual machine's public IP or private IP address?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Public IP",
                    "text": "Public IP"
                },
                {
                    "value": "Private IP",
                    "text": "Private IP"
                }
            ],
            "required": false
        },
        {
            "id": "ippublic",
            "order": 4,
            "visibility": "ippublicprivate == Public IP",
            "controlType": "dropdown",
            "displayLabel": "Can you connect to the private IP?",
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
            "id": "ipprivate",
            "order": 5,
            "visibility": "ippublicprivate == Private IP",
            "controlType": "dropdown",
            "displayLabel": "Can you connect to the public IP?",
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
                    "value": "The virtual machine does not have a public IP",
                    "text": "The virtual machine does not have a public IP"
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
