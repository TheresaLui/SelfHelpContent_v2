<properties
         pageTitle="Scoping questions for New Project Creation and Addition of Tool"
         description="Scoping questions for New Project Creation and Addition of Tool"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675740"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="151371b2-3680-444e-b486-aee15158472c"
	ownershipId="Compute_AzureMigrate"
/>

# Creating a new project and adding a tool

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Creating a new project and adding a tool",
    "fileAttachmentHint": "",
    "formElements": [
         {
            "id": "geography_selection",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the geography where you are trying to deploy the project:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Asia",
                    "text": "Asia"
                },
                {
                    "value": "Europe",
                    "text": "Europe"
                },
                {
                    "value": "United Kingdom",
                    "text": "United Kingdom"
                },
                {
                    "value": "United States",
                    "text": "United States"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
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
