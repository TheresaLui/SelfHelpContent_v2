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
            "id": "problem_start_time",
            "order": 1,
            "controltype": "datetimepicker",
            "displayLabel": "When did you face this question?",
            "required": true
        },
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
