<properties
	pageTitle="Issue shaping enrichment for knowledge store"
	description="Issue shaping enrichment for knowledge store"
	authors="dereklegenzoff"
	ms.author="delegenz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681360"
	productPesIds="15568"
	cloudEnvironments="Public, FairFax, usnat, ussec"
	schemaVersion="1"
	articleId="316f28a3-0080-4b72-ae58-cb7d9dc43603"
	ownershipId="AzureSearch_AzureSearch"
/>

# Issue shaping enrichment for knowledge store
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Issue shaping enrichment for knowledge store",
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
            "displayLabel": "When did you last try to run the indexer?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---