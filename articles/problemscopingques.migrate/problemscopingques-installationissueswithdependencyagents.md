<properties
         pageTitle="Scoping questions for installation issues with dependency agents"
         description="Scoping questions for installation issues with dependency agents"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675753"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="66fd8479-a4a5-42e1-a0c0-4864b6adefd2"
	ownershipId="Compute_AzureMigrate"
/>

# Installation issues with dependency agents

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Installation issues with dependency agents",
    "fileAttachmentHint": "",
    "formElements": [
         {
            "id": "VM_Type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which type of VM are you trying to install on?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Windows",
                    "text": "Windows"
                },
                {
                    "value": "Linux",
                    "text": "Linux"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "OS_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of the OS",
            "watermarkText": "E.g. Windows Server 2003",
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
    ],
    "$schema": "SelfHelpContent"
}
---
