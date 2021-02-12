<properties
    pageTitle="Replication"
    description="Replication"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747621,32747626"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-flexsvr-replication-issues"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Replication - Issues to Azure Database for MySQL
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Issues of Azure MySQL replication",
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
            "id": "master_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the server name and region of your master server?",
            "required": false
        },
        {
            "id": "replica_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the server name and region of your replica server?",
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
