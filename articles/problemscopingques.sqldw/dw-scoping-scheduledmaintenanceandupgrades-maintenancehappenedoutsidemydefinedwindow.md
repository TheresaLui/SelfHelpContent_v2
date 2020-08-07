<properties
	articleId="dw-scoping-scheduledmaintenanceandupgrades-maintenancehappenedoutsidemydefinedwindow.md"
	pageTitle="Maintenance happened outside of my defined window"
	description="Maintenance happened outside of my defined window"
	authors="mlee3gsd"
	ms.author="martinle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635203"
	productPesIds="15818"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Scheduled Maintenance and Upgrades - Maintenance happened outside of my defined window
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Maintenance happened outside of my defined window",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the maintenance occur?",
            "required": true
        },
        {
            "id": "dw_scoping_sched_slo",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the performance tier of the data warehouse at the time of the maintenance event?",
            "required": false
        },
        {
            "id": "dw_scoping_sched_region",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the region of your data warehouse?",
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