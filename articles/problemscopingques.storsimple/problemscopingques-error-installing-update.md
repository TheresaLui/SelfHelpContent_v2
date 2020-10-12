<properties
	articleId="10ed438a-9624-4f7e-8ea8-7e62906af8dc"
	pageTitle="Scoping error installing update"
	description="Error installing update"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630501"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Error installing update
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Error installing update",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "update_type",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which update installation is failing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Software",
                    "text": "Software"
                },
                {
                    "value": "Firmware",
                    "text": "Firmware"
                }
            ],
            "required": false
        },
        {
            "id": "update",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How is the update being installed?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "From Azure Portal",
                    "text": "From Azure Portal"
                },
                {
                    "value": "As a hotfix",
                    "text": "As a hotfix"
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
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include output."
                },
                {
                    "text": "Run `invoke-hcsdiagnostics -scope network` and provide output below to assist in troubleshooting the issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
