<properties
    pageTitle="Replication"
    description="Replication"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747583"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-gen1-migration-restore"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Migration - Restore from MySQL dump
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Restore from MySQL dump",
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
            "id": "source_server_location",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Where is dump file?",
            "required": false
        },
        {
            "id": "error",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What error did you see when restore?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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
