<properties
         pageTitle="Scoping questions for Test Migration"
         description="Scoping questions for Test Migration"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675759"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="114d28f4-3a14-4c48-b338-76f5b223aa1e"
	ownershipId="Compute_AzureMigrate"
/>

# Test Migration

---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Test Migration",
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
                    "text": "Don't know"
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
