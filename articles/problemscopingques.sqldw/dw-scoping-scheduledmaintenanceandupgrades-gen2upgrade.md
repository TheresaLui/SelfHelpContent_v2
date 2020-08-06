<properties
        articleId="dw-scoping-scheduledmaintenanceandupgrades-gen2upgrade.md"
        pageTitle="Gen2 upgrade from Gen1"
        description="Gen2 upgrade from Gen1"
        authors="mlee3gsd"
        ms.author="martinle"
        selfHelpType="problemScopingQuestions"
        supportTopicIds="32635200"
        productPesIds="15818"
        cloudEnvironments="public, Fairfax, usnat, ussec"
        schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Scheduled Maintenance and Upgrades - Gen2 upgrade from Gen1

---

{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "SQL DW Gen2 upgrade from Gen1",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "dw_scoping_gen2upgrade_region",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What region is your data warehouse?",
            "required": false
        },
        {
            "id": "dw_scoping_gen2upgrade_selfupgrade",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Are you self-upgrading to Gen2?",
            "required": false
        },
	{
            "id": "dw_scoping_gen2upgrade_error",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "If an error was displayed, what was the error message?",
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
