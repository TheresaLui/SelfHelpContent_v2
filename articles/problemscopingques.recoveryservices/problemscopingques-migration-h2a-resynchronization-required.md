<properties
         pageTitle="Scoping questions for Hyper-V VM resynchronization failure"
         description="Scoping questions for Hyper-V VM  resynchronization failure"
         authors="ashishgangwar, TobyTu"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680620"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	     articleId="9249efab-1e0d-401c-aa50-6dd5fee36857"
	ownershipId="Compute_SiteRecovery"
/>

# Questions Hyper-V VM resynchronization failure

---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "Resynchronization required for VM",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide name of the VM you are facing issues with",
            "watermarkText": "Enter name(s) to scope down quickly",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID or job ID of the add or register operation",
            "watermarkText": "Enter in the error ID or job ID",
            "infoBalloonText": "Click on the VM in the replicated items list, view and paste the error code shown for the VM(s)",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I had been protecting the VM successfully, but",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "The VM is marked as critical with resynchronization required error",
                    "text": "The VM is marked as critical with resynchronization required error"
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
