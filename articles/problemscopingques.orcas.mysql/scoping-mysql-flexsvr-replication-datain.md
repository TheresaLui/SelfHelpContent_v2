<properties
    pageTitle="Replication"
    description="Replication"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747633"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-flexsvr-replication-data_in"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Replication - Data-in replication to Azure Database for MySQL
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
