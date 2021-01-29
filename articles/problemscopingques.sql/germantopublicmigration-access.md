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
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "sqlexception_received_on_client",
            "order": 20,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide subscription pairs for allow listing. (Obscure the personally identifiable information.)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Migration Details",
            "watermarkText": "Provide source (Azure Germany) and target (Azure Global) subscription IDs to enable the geo-replication method to migrate your database.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
