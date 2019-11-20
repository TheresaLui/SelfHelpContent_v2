<properties
         pageTitle="Scoping questions for resynchronization required for VM"
         description="Scoping questions for resynchronization required for VM"
         authors="TobyTu"
         ms.author="aaronmax"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680620"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="q2ade910-df87-4222-9534-98223c9c0527"
/>

# Resynchronization required for VM
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
            "watermarkText": "Click on the VM in the replicated items list, view and paste the error code shown for the VM(s)",
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
            "watermarkText": "Enter local time",
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
