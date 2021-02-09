<properties
	articleId="f4b6acbe-89ce-4879-b6aa-ae09564094d2"
	pageTitle="Scoping Questions for Purview Missing classifications on an asset or classification report is empty"
	description="Scoping Questions for Purview Missing classifications on an asset or classification report is empty"
	authors="deeptivu"
	ms.author="deeptivu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783246,32783217"
	productPesIds="17354"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_ProjectBabylon"
/>
# Purview Missing classifications on an asset
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Purview Missing classifications on an asset",
    "fileAttachmentHint": "Share screenshot of your scan rule set that shows the classifications you are trying to match. If you are using custom classification, share a screenshot of the custom classification definition",
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
            "id": "data_source",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "What data source are you scanning?",
            "required": false
        },
        {
            "id": "sample_item",
            "order": 50,
            "controlType": "textbox",
            "displayLabel": "Share a sample item from the scanned data source that you think should match",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
