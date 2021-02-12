<properties
         pageTitle="Scoping questions for add or register a Hyper-V Server"
         description="Scoping questions for add or register a Hyper-V Server"
         authors="TobyTu"
         ms.author="aaronmax"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32536385"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="q2ade909-df87-4222-9534-98223c9c0527"
	ownershipId="Compute_SiteRecovery"
/>

# Add or register a Hyper-V Server
---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "Add or register a Hyper-V Server",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "host_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide name of the Hyper-V host you are trying to add",
            "watermarkText": "Enter name(s) to scope down quickly",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID or job ID of the add or register operation",
            "watermarkText": "Enter in the error ID or job ID",
            "infoBalloonText": "Open a new tab, navigate to Recovery Services Vault, click on Jobs & paste error or job ID of failed job",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I am trying to register a new Hyper-V host, but",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I am unable to install the provider on the Hyper-V host",
                    "text": "I am unable to install the provider on the Hyper-V host"
                },
                {
                    "value": "I am unable to see the Host after installing the provider",
                    "text": "I am unable to see the Host after installing the provider"
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
                    "value": "Prepare on-premises Hyper-V servers for disaster recovery to Azure",
                    "text": "Prepare on-premises Hyper-V servers for disaster recovery to Azure"
                },
                {
                    "value": "Troubleshoot Hyper-V to Azure replication and failover",
                    "text": "Troubleshoot Hyper-V to Azure replication and failover"
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
