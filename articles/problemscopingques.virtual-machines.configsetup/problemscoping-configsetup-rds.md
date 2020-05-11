<properties
                pageTitle="Configuration and Setup"
                description="Configuration and Setup"
                authors="summertgu"
                ms.author="tiag"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32411854"
                productPesIds="14749"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b4b6273d-558e-4f2d-ab00-36a830ea0083"
	ownershipId="Compute_VirtualMachines_Content"
/>
# Config and Setup
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Create RDS in Azure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "opreation_rds",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What are you trying to do?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create the RDS",
                    "text": "Create the RDS"
                },
                {
                    "value": "Configure the RDS",
                    "text": "Configure the RDS"
                },
                {
                    "value": "Manage the RDS",
                    "text": "Manage the RDS"
                }
            ],
            "required": false
        },
        {
            "id": "config_storage",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are your VMs using Standard Storage or Premium Storage?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Standard Storage",
                    "text": "Standard Storage"
                },
                {
                    "value": "Premium Storage",
                    "text": "Premium Storage"
                }
            ],
            "required": false
        },
        {
            "id": "upd_store",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Where would the UPD be stored?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "This local machine",
                    "text": "This local machine"
                },
                {
                    "value": "Configured remotely",
                    "text": "Configured remotely"
                }
            ],
            "required": false
        },
        {
            "id": "app_cluster",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Are there any other application or clusters configured on this server?",
            "useAsAdditionalDetails": true,
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
