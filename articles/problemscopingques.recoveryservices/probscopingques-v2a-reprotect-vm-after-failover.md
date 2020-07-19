<properties
         pageTitle="Scoping questions for reprotect VMware VM after failover"
         description="Scoping questions for reprotect VMware VM after failover"
         authors="ashishgangwar, TobyTu"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32536447"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	     articleId="379e6c2e-980b-45a3-a272-b88b13e39d08"
	ownershipId="Compute_SiteRecovery"
/>

# Reprotect VM after failover

---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "Reprotect VM after failover",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide name of the VM to re-protect",
            "watermarkText": "Enter name(s) to scope down quickly",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID or job ID of the re-protect operation",
            "watermarkText": "Enter in the error or job ID",
            "infoBalloonText": "Open a new tab, navigate to Recovery Services Vault, click on Jobs & paste error or job ID of failed re-protect job",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I am trying to re-protect, but",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "I am unable to select data store for re-protect",
                    "text": "I am unable to select data store for re-protect"
                },
                {
                    "value": "I am unable to select master target server",
                    "text": "I am unable to select master target server"
                },
                {
                    "value": "I am unable to set up process server in Azure",
                    "text": "I am unable to set up process server in Azure"
                },
                {
                    "value": "I am not able to boot or see all disks after failback",
                    "text": "I am not able to boot or see all disks after failback"
                },
                {
                    "value": "My original vCenter is not available",
                    "text": "My original vCenter is not available"
                },
                {
                    "value": "My original configuration server is not available",
                    "text": "My original configuration server is not available"
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
