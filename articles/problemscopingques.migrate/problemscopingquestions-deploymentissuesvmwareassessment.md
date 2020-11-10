<properties
    pageTitle="Scoping questions for deployment issues with Azure Migrate appliance for VMware (Server Assessment)"
    description="Scoping questions for deployment issues with Azure Migrate appliance for VMware (Server Assessment)"
    authors="An-mol"
    ms.author="anvar"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32675747"
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="16626ec8-bb1d-4ed4-baf2-9d659b578d89"
	ownershipId="Compute_AzureMigrate"
/>

# Deployment issues with Azure Migrate appliance for VMware

---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Deployment issues with Azure Migrate appliance for VMware",
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
                    "value": "Creating the appliance VM",
                    "text": "Creating the appliance VM"
                },
                {
                    "value": "Pre-requisites and Setup",
                    "text": "Pre-requisites and Setup"
                },
                {
                    "value": "Registration with Azure Migrate project",
                    "text": "Registration with Azure Migrate project"
                },
                 {
                    "value": "Connecting with the vCenter Server",
                    "text": "Connecting with the vCenter Server"
                },
                 {
                    "value": "Save and Start Discovery",
                    "text": "Save and Start Discovery"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
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
