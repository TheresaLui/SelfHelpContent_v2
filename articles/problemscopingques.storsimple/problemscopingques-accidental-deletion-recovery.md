<properties
	articleId="d9bddde6-4c5b-49ad-99c2-c54e952b6d91"
	pageTitle="Scoping for accidental deletion and recovery"
	description="Accidental deletion and recovery scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630492"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Accidental deletion and data recovery
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Accidental deletion and recovery",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "deleted_component",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which component has been deleted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Volume Container",
                    "text": "Volume Container"
                },
                {
                    "value": "Volume",
                    "text": "Volume"
                },
                {
                    "value": "Storage Account",
                    "text": "Storage Account"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "recovery",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you tried to clone or restore from backups?",
            "watermarkText": "Choose an option",
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
                    "value": "Not Applicable",
                    "text": "Not Applicable"
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
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
