<properties
	pageTitle="Azure-SSIS Provision and Configuration Info"
	description="Scoping questions to gather Azure Data Factory SSIS IR information"
	authors="chez-charlie"
	ms.author="chez"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32680894,32680895,32680896"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="9543B0E5-DAD6-4405-8B33-C5DEC75F375B"
	ownershipId="AzureData_DataFactory"
/>

# Azure-SSIS Provision and Configuration Info

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure-SSIS Provision and Configuration Info",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Is it a new issue or regression?"
                },
                {
                    "text": "Is the issue intermittent or persistent?"
                }
            ]
        },
        {
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you see?",
            "required": false
        },
        {
            "id": "data_factory_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What's the name of Data Factory?",
            "required": false
        },
        {
            "id": "ssisir_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's the name of Azure-SSIS Integration Runtime?",
            "required": false
        },
        {
            "id": "operation_trigger",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Where do you trigger the operation? Did you use ADF Portal or SDK?",
            "dropdownOptions": [
                {
                    "value": "ADF Portal",
                    "text": "ADF Portal"
                },
                {
                    "value": "PowerShell",
                    "text": "PowerShell"
                },
                {
                    "value": ".NET Client",
                    "text": ".NET Client"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not applicable"
                }
            ],
            "required": true
        },
		{
			"id": "Activity_id",
            "order": 6,
			"controlType": "textbox",
			"displayLabel": "Please provide the the ActivityID of the operation. (you can find it at the bottom of the error message dispalyed on the portal)",
			"required": false
		},
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
