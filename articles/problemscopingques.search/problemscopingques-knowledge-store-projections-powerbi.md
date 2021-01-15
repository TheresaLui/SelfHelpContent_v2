<properties
	pageTitle="Issue accessing a projection in Power BI"
	description="Issue accessing a projection in Power BI"
	authors="dereklegenzoff"
	ms.author="delegenz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681377"
	productPesIds="15568"
	cloudEnvironments="Public, FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="82a10aa4-1215-4a69-86c0-7d8c74e37d0b"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue accessing a projection in Power BI
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Issue accessing a projection in Power BI",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "indexer_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the name of your indexer?",
            "required": true,
            "useAsAdditionalDetails": false
        },
        {
            "id": "skillset_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the name of your skillset?",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did you last run the indexer to create the projections?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---