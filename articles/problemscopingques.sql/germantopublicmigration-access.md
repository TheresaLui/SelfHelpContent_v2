<properties
	articleId="dcf3cdb4-0b18-46f2-a834-518db33c300a"
	pageTitle="SQL Database"
	description="Scoping questions for Migration from Microsoft Cloud Germany to global Azure"
	authors="subbuk"
	authoralias="subbuk"
	ms.author="subbuk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32785509, 32785645"
	productPesIds="13491, 15660"
	cloudEnvironments="blackForest"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# SQL Database
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "SQL Database",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Date (Optional)",
            "required": false
        },
				{
						"id": "problem_description",
						"order": 1000,
						"controlType": "multilinetextbox",
						"displayLabel": "Description",
						"watermarkText": "Provide your target (Azure Global) Subscription IDs for listing to allow Geo-Replication method of database migration.",
						"required": true,
						"useAsAdditionalDetails": true
				}
    ]
}
---
