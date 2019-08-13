<properties
         pageTitle="Scoping questions for not able to connect to VM"
         description="Scoping questions for not able to connect to VM"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680617"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="6b342a85-0813-4b4d-b7d0-43639892e013"
/>
# Questions on not able to connect to VM after Failover 

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "V2A - not able to connect to VM",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed Site Recovery job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
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
    ]
}
---
