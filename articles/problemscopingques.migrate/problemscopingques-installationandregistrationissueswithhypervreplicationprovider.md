<properties
         pageTitle="Scoping questions for installation and registration issues with Hyper-V replication provider"
         description="Scoping questions for installation and registration issues with Hyper-V replication provider"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675752"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="2f0b09b6-7ee1-4f4e-95fa-560d385b0c7b"
	ownershipId="Compute_AzureMigrate"
/>

# Installation and registration issues with Hyper-V replication provider

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Installation and registration issues with Hyper-V replication provider",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "Whitelisting_URLs",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Have you whitelisted the URLs?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
        },
        {
            "id": "ports_opened",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are the required ports open?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
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
