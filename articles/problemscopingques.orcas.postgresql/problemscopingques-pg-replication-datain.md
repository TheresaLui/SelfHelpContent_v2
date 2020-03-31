<properties
    pageTitle="Replication"
    description="Replication"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640007"
    productPesIds="16222"
    cloudEnvironments="public, Fairfax"
    schemaVersion="1"
    articleId="problemscopingques-pg-replication-data_in"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Replication - Data-in replication to Azure Database for PG
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Replication Data-in Replication",
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
            "displayLabel": "Where is the source server? For example, AWS, on-prem on Azure or other cloud services",
            "required": false
        },
        {
            "id": "source_server_load",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "How large the load is on source server?",
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
