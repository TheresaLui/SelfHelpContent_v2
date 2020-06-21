<properties
	articleId="dw-scoping-backuprestoreandbusinesscontinuity-recoverdroppedserverorresourcegroup.md"
	pageTitle="Recover dropped server or resource group"
	description="Recover dropped server or resource group"
	authors="anumjs"
	ms.author="anjangsh"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635215"
	productPesIds="15818"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Backup, restore and business continuity - recover dropped server or resource group
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Recover dropped server or resource group",
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
            "id": "dw_scoping_server_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the dropped server name?",
            "required": false
        },
        {
            "id": "dw_scoping_restore_region",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What region is the dropped server in?",
            "required": false
        },
        {
            "id": "dw_scoping_resource_group_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the dropped resource group name?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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