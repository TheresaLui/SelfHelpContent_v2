<properties
         pageTitle="Scoping questions for VMware to Azure vCenter issues and queries"
         description="Scoping questions for VMware to Azure vCenter issues and queries"
         authors="ashishgangwar"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32536387"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
	     articleId="a3a4bbf7-0f9f-40e9-8834-682466a42523"
/>
# Questions for VMware to Azure vCenter issues and queries
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "vCenter issues and queries",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide vCenter name",
            "watermarkText": "Enter the name of the VMware vCenter",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed Site Recovery job Activity ID if applicable:",
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
