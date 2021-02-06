<properties
	articleId="b8e8c724-96e7-43e9-b85b-e34fa1df8533"
	pageTitle="Scoping Questions for Purview - I do not see any changes to the related resources"
	description="Scoping Questions for Purview - I do not see any changes to the related resources"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783235"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview - I do not see any changes to the related resources
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview - I do not see any changes to the related resources",
    "fileAttachmentHint": "In case it’s a custom classification, please add screenshot of the configured classification",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
         {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Brief description of the issue",
            "watermarkText": "Please provide any information related to this issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "catalog_name",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "What is the name of the catalog?",
            "required": false
        },
        {
            "id": "new_values",
            "order": 50,
            "controlType": "textbox",
            "displayLabel": "What are the new values put in for the scoped resource set policy?",
            "required": false
        },
        {
            "id": "added_time",
            "order": 60,
            "controlType": "textbox",
            "displayLabel": "When are the new values added?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
