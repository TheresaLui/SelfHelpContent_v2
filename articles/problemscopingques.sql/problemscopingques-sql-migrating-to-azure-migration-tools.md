<properties
	pageTitle="Migration tools"
	description="Scoping questions to capture more details about migration tools"
	authors="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630433"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-migrating-migration-tools"
	ownershipId="AzureData_AzureSQLDB"
/>
# scoping questions for migration tools
---
{
	"$schema": "SelfHelpContent",
	"resourceRequired": false,
	"subscriptionRequired": false,
	"title": "Migration tools",
	"formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
    {
            "id": "Tool_dropdown",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the tool being used?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the tool being used",
	    "dropdownOptions": [
	    	{
                    "value": "DEA",
                    "text": "Database Experimentation Assistant"
                },
		{
                    "value": "DMA",
                    "text": "Data Migration Assistant (DMA)"
                },
                {
                    "value": "DMS",
                    "text": "Database Migration Service (DMS)"
                },
                {
                    "value": "BACPAC",
                    "text": "Export and Import BACPAC files"
                },
                {
                    "value": "SSMA",
                    "text": "SQL Server Migration Assistant"
                },
                {
                    "value": "repl",
                    "text": "Transaction replication"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer or other answer"
                }
            ],
            "required": true
        },
    {
            "id": "engine_source",
            "order": 3,
            "controlType": "dropdown",
            "visibility": "Tool_dropdown == SSMA",
            "displayLabel": "What is the DB engine source?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the DB engine source",
	    "dropdownOptions": [
                {
                    "value": "Access",
                    "text": "Access"
                },
                {
                    "value": "DB2",
                    "text": "DB2"
                },
                {
                    "value": "MySQL",
                    "text": "MySQL"
                },
                {
                    "value": "ORACLE",
                    "text": "Oracle"
                },
                {
                    "value": "SAPASE",
                    "text": "SAP ASE"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know the answer"
                }
            ],
            "required": false
        },
	{
            "id": "tool_version",
            "order": 4,
            "controlType": "textbox",
	          "visibility": "Tool_dropdown == DMA || Tool_dropdown == SSMA || Tool_dropdown == DEA || Tool_dropdown == BACPAC",
            "displayLabel": "What is the tool version?",
            "infoBalloonText": "Enter the tool version being used",
            "required": false
        },
    {
            "id": "source",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Where is located the source DB or BACPAC file?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Choose the source location",
	    "dropdownOptions": [
                {
                    "value": "Storage",
                    "text": "Azure Storage"
                },
                {
                    "value": "VM",
                    "text": "Azure VM"
                },
                {
                    "value": "external",
                    "text": "On-premises or another Cloud supplier"
                }
            ],
            "required": false
        },
	{
            "id": "size",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is the size of the original DB?",
            "infoBalloonText": "Enter the size of the original database.",
            "required": false
        },
    {
            "id": "downtime",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What is the max downtime allowed?",
            "infoBalloonText": "Enter the max downtime allowed for the migration",
            "required": false
        },
    {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error you are receiving. If available,please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
