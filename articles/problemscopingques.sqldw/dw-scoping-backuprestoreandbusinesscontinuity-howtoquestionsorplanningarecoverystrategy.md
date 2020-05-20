<properties
	articleId="dw-scoping-backuprestoreandbusinesscontinuity-howtoquestionsorplanningarecoverystrategy.md"
	pageTitle="How-to questions or planning a recovery strategy"
	description="How-to questions or planning a recovery strategy"
	authors="mlee3gsd"
	ms.author="martinle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635201"
	productPesIds="15818"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Backup, Restore and Business Continuity - How-to questions or planning a recovery strategy
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "How-to questions or planning a recovery strategy",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
	{
            "id": "dw_scoping_backup_backupregion",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the region of your data warehouse?",
            "required": false
        },
        {
            "id": "dw_scoping_backup_slo",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the performance tier of your data warehouse?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
