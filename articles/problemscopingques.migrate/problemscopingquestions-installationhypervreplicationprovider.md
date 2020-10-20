<properties
    pageTitle="Scoping questions for deployment issues with Hyper-V Replication Provider"
    description="Scoping questions for deployment issues with Hyper-V Replication Provider"
    authors="An-mol"
    ms.author="anvar"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32755161"
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="16626ewq-bb1d-4ed4-baf2-9d659b578d89"
	ownershipId="Compute_AzureMigrate"
/>

# Installing the Hyper-V replication provider

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Installing the Hyper-V replication provider",
    "fileAttachmentHint": "",
    "formElements": [
             {
            "id": "failed_step",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the step that failed",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Registration with Azure Migrate project",
                    "text": "Registration with Azure Migrate project"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
            },
         {
            "id": "appliance_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of affected Hyper-V hosts",
            "watermarkText": "E.g. MyContosoHost",
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
