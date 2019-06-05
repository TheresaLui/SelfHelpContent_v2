<properties
         pageTitle="Scoping questions for  VMM server addition failure"
         description="Scoping questions for VMM server addition failure"
         authors="ashishgangwar"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32634432"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
	     articleId="881fcef2-0569-437b-bcda-0eede66b5dd1"
/>
# Questions  VMM server addition failure 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "VMM server addition failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which VMM server is experiencing the problem?",
            "watermarkText": "Enter the name of the VMM server",
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
