<properties
    pageTitle="Scoping questions for deployment issues with Azure Migrate appliance for VMware"
    description="Scoping questions for deployment issues with Azure Migrate appliance for VMware"
    authors="An-mol"
    ms.author="anvar"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32675748"
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="c3178863-02c4-4abc-90bc-a296cf55f14c"
	ownershipId="Compute_AzureMigrate"
/>

# Deployment issues with Azure Migrate appliance for VMware

---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Deployment issues with Azure Migrate appliance for VMware",
    "fileAttachmentHint": "",
    "formElements": [
             {
            "id": "replication_scenarios",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the replication scenario",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Agent based replication",
                    "text": "Agent based replication"
                },
                {
                    "value": "Agent less replication",
                    "text": "Agent less replication"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "required": true
            },
            {
            "id": "step_failed",
            "order": 2,
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
                    "value": "Connection with vCenter Server",
                    "text": "Connection with vCenter Server"
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
            "order": 3,
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
            "order": 4,
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
            "order": 5,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the name of appliance(s) (if applicable)",
            "watermarkText": "E.g. MyContosoAppliance",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
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
