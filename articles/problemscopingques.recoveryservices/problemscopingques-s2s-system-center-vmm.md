<properties
         pageTitle="Scoping questions for System Center VMM to System Center VMM"
         description="Scoping questions for System Center VMM to System Center VMM"
         authors="TobyTu"
         ms.author="aaronmax"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32634430"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="q2ade912-df87-4222-9534-98223c9c0527"
	ownershipId="Compute_SiteRecovery"
/>

# System Center VMM to System Center VMM
---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "System Center VMM to System Center VMM",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "issue_summary",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide a summary of the issue you are having with site to site replication using VMM",
            "watermarkText": "Enter a summary of the issue",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID or job ID of the add or register operation",
            "watermarkText": "Enter in the error or job ID",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I am having issue with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Registering VMM",
                    "text": "Registering VMM"
                },
                {
                    "value": "Enabling replication",
                    "text": "Enabling replication"
                },
                {
                    "value": "Failover",
                    "text": "Failover"
                },
                {
                    "value": "Failback",
                    "text": "Failback"
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
                    "value": "Support matrix for disaster recovery of Hyper-V VMs to a secondary site",
                    "text": "Support matrix for disaster recovery of Hyper-V VMs to a secondary site"
                },
                {
                    "value": "Set up logical networks in the VMM fabric",
                    "text": "Set up logical networks in the VMM fabric"
                },
                {
                    "value": "Fail over VMs and physical servers",
                    "text": "Fail over VMs and physical servers"
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
