<properties
	articleId="problemscopingques-sqlmi-backup-restore-bc-planning-recovery-strategy"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions about how to questions or planning a recovery strategy"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
   	productPesIds="16259"
	supportTopicIds="32637266"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "How to questions or planning a recovery strategy",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "type_question",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "What is the topic you need clarification?",
            "dropdownOptions": [
                {
                    "value": "architecture",
                    "text": "High Availability Architecture"
                },
                {
                    "value": "backups",
                    "text": "Backups"
                },
                {
                    "value": "replication",
                    "text": "Replication"
                },
                {
                    "value": "recover",
                    "text": "Recover a database or instance"
                },
                {
                    "value": "drill",
                    "text": "Disaster Recovery Drill or Application connectivity resiliency"
                },
                {
                    "value": "dont_know_answer",
                     "text": "Don't know, other topic or several of the previous topics"
                }
            ],
            "required": true
        },
        {
            "id": "backups",
            "order": 20,
            "controlType": "dropdown",
            "visibility": "type_question == backups",
            "displayLabel": "What kind of backups?",
            "dropdownOptions": [
                {
                    "value": "auto",
                    "text": "Automated Backups"
                },
                {
                    "value": "native",
                    "text": "Native Backup to BLOB storage"
                },
                {
                    "value": "ltr",
                    "text": "Long-Term Retention Backups"
                },
                {
                    "value": "dont_know_answer",
                     "text": "Don't know or several of the previous options"
                }
            ],
            "required": true
        },
        {
            "id": "replication",
            "order": 30,
            "controlType": "dropdown",
            "visibility": "type_question == replication",
            "displayLabel": "What kind of data replication?",
            "dropdownOptions": [
                {
                    "value": "active",
                    "text": "Active Geo-Replication"
                },
                {
                    "value": "groups",
                    "text": "Auto Failover Groups"
                },
                {
                    "value": "trans_repl",
                    "text": "Transaction Replication"
                },
                {
                    "value": "dont_know_answer",
                     "text": "Don't know or several of the previous options"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your request",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
