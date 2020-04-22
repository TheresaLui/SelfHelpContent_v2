<properties
    pageTitle="Database Backup Restore"
    description="Database Backup Restore"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640087"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-mysql-backuprestore-recover_droppedresource"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Backup, Restore and Business Continuity - Recover A Dropped Resource
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Recover Dropped Resource",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "subscription_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is your subscription ID?",
            "required": false
        },
        {
            "id": "resource_group_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the resource group name of the dropped server?",
            "required": false
        },
        {
            "id": "dropped_server_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the server name of the dropped server?",
            "required": false
        },
        {
            "id": "drop_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did you drop the server? ",
            "required": true
        },
        {
            "id": "guarantee_recovered",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "There is no guarantee the data can be recovered to latest point. Do you accept?",
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
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
