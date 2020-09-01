<properties
         pageTitle="Scoping questions for deployment issues with Azure Migrate appliance for Hyper-V"
         description="Scoping questions for deployment issues with Azure Migrate appliance for Hyper-V"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675746"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="bbf20fea-7a20-4522-a96a-01bae88f225f"
	ownershipId="Compute_AzureMigrate"
/>

# Deployment issues with Azure Migrate appliance for Hyper-V

---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Deployment issues with Azure Migrate appliance for Hyper-V",
    "fileAttachmentHint": "",
    "formElements": [
         {
            "id": "step_failed",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the step that is failing",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Creation of Appliance VM",
                    "text": "Creation of Appliance VM"
                },
                {
                    "value": "Pre-requisites and setup",
                    "text": "Pre-requisites and setup"
                },
                {
                    "value": "Registration with Azure Migrate Project",
                    "text": "Registration with Azure Migrate Project"
                },
                {
                    "value": "Addition/validation of Hyper-V hosts",
                    "text": "Addition/validation of Hyper-V hosts"
                },
                {
                    "value": "Save and start discovery",
                    "text": "Save and start discovery"
                },
 {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "Whitelisting_URLs",
            "order": 2,
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
                }
            ],
            "required": false
        },
        {
            "id": "ports_opened",
            "order": 3,
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
            "id": "appliance_name",
            "order": 4,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of appliance(s) (if applicable)",
            "watermarkText": "E.g. MyContosoAppliance",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
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
    ],
    "$schema": "SelfHelpContent"
}
---
