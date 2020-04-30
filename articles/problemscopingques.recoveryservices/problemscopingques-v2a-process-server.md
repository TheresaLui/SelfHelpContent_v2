<properties
         pageTitle="Scoping questions for Process server deployment and issues"
         description="Scoping questions for Process server deployment and issues"
         authors="TobyTu"
         ms.author="aaronmax"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32536429"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="q2ade903-df87-4222-9534-98223c9c0527"
	ownershipId="Compute_SiteRecovery"
/>

# Process server deployment and issues
---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "Process server deployment and issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "server_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide name of the process server you are facing issues with",
            "watermarkText": "Enter name of process server",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID of the process server",
            "watermarkText": "Enter in the error ID",
            "infoBalloonText": "Open a new tab, Open a new tab, navigate to Recovery Services Vault, paste the error code seen for the process server in the overview blade",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Choose the action you are having trouble with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "My process server is unhealthy after upgrade",
                    "text": "My process server is unhealthy after upgrade"
                },
                {
                    "value": "Unable to setup a new process server",
                    "text": "Unable to setup a new process server"
                },
                {
                    "value": "Process server is not connected to ASR services",
                    "text": "Process server is not connected to ASR services"
                },
                {
                    "value": "Process server is in a critical state",
                    "text": "Process server is in a critical state"
                },
                {
                    "value": "Unable to select process server during enable replication",
                    "text": "Unable to select process server during enable replication"
                },
                {
                    "value": "Switch/load balance process server",
                    "text": "Switch or load balance process server"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "tried_steps",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "I have gone through steps provided in the following articles",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Monitor process servers",
                    "text": "Monitor process servers"
                },
                {
                    "value": "Troubleshoot process servers",
                    "text": "Troubleshoot process servers"
                },
                {
                    "value": "Manage process servers",
                    "text": "Manage process servers"
                },
                {
                    "value": "Manage Site Recovery updates",
                    "text": "Manage Site Recovery updates"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
       {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "watermarkText": "Enter in local time",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ]
}
---
