<properties
    pageTitle="Scoping questions for Replication issues"
    description="Scoping questions for Replication issues"
    authors="An-mol"
    ms.author="anvar"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32675757"
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="b3f6e26c-0cc9-48c0-a848-397038546515"
	ownershipId="Compute_AzureMigrate"
/>

# Replication issues

---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Replication issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "server_kind",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What kind of servers are you trying to replicate?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "VMware VMs",
                    "text": "VMwareVMs"
                },
                {
                    "value": "Hyper-V VMs",
                    "text": "Hyper-V VMs"
                },
                {
                    "value": "Physical Server",
                    "text": "Physical Server"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "if_VMware_method",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "If you are selecting VMware VMs, please provide the method for replication",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Agent based",
                    "text": "Agent based"
                },
                {
                    "value": "Agent less",
                    "text": "Agent less"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
