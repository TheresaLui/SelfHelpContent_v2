<properties
         pageTitle="Scoping questions for count mismatch on Azure Migrate Dashboard"
         description="Scoping questions for count mismatch on Azure Migrate Dashboard"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675737"
         productPesIds="16348"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="275455e6-9c0f-43fa-9459-b011230d20fd"
/>

# Count mismatch on Azure Migrate dashboard

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Count mismatch on Azure Migrate dashboard",
    "fileAttachmentHint": "",
    "formElements": [
         {
            "id": "tool_used",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the tool you are using:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Azure Migrate: Server Assessment",
                    "text": "Azure Migrate: Server Assessment"
                },
                {
                    "value": "Azure Migrate: Server Migration",
                    "text": "Azure Migrate: Server Migration"
                },
                {
                    "value": "Carbonite",
                    "text": "Carbonite"
                },
                {
                    "value": "Cloudamize",
                    "text": "Cloudamize"
                },
                {
                    "value": "Corent Technology",
                    "text": "Corent Technology"
                },
                {
                    "value": "Device42",
                    "text": "Device42"
                },
                {
                    "value": "Turbonomic",
                    "text": "Turbonomic"
                },
                {
                    "value": "UnifyCloud"
                    "text": "UnifyCloud"
                },
{
                    "value": "Other"
                    "text": "Other"
                }
            ],
            "required": true
        },
         {
            "id": "countmismatch_metric",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Which metric does not match?",
            "watermarkText": "E.g. Discovered Servers",
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
