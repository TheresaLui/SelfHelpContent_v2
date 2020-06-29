<properties
	pageTitle="Import from BACPAC"
	description="Scoping questions to capture more details about issues while trying Import from BACPAC"
	authors="andikshi,vitomaz-msft,MladjoA"
	ms.author="vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32637268"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sqlmi-importexportreplication-importfrombacpac"
	ownershipId="AzureData_AzureSQLMI"
/>
# Import from BACPAC to create SQL DB MI
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
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
            "id": "platform_type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What tool or method are you using to import?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Select one of the following",
            "dropdownOptions": [
                {
                    "value": "SSMS",
                    "text": "SSMS"
                },
                {
                    "value": "SqlPackage",
                    "text": "SqlPackage.exe"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "version_details",
            "order": 5,
            "controlType": "textbox",
            "visibility": "platform_type == SSMS || platform_type == SqlPackage",
            "displayLabel": "Please provide the version details",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Please provide the full error that you are seeing or explain your issue in detail.If available, please attach any relevant screenshots and scripts that you have used."
        }
    ]
}
---
