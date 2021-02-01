<properties
	pageTitle="Azure Data Movement connectivity and connectors"
	description="Scoping questions to gather Azure Data Movement connectivity issue information"
	authors="hecepeda"
	ms.author="hecepeda"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32784316,32784317,32784318,32784319,32784320,32784321,32784322"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="adms-connectivity.md"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Movement Issue

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Movement copy issue info",
    "fileAttachmentHint": "Please attach JSON code for dataset, linked service and screen shots to help us triage your problem faster",
    "diagnosticCard": {
        "title": "Azure Copy Activity Troubleshooter",
        "description": "Our Copy Activity RunId Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect the issues we were looking for in your resource. Refer to the help manual below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please briefly describe the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [{"text": "Is it a new issue or regression?"}, {"text": "Is the issue intermittent or persistent?"}]
        },
        {
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you see?",
            "required": false
        },
        {
            "id": "radio_servertype",
            "order": 3,
            "controlType": "radioButtonGroup",
            "displayLabel": "Select whether you are trying to reach the source or sink server:",
            "radioButtonOptions": [{
                    "value": "Source",
                    "text": "Source server"
                }, {
                    "value": "Sink",
                    "text": "Sink server"
                }
            ],
            "required": true
        },
        {
            "id": "connector_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What connector are you using?",
            "required": false
        },
		{
            "id": "problem_run_id",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Is this a run time issue? If yes, Provide the Pipeline or Activity RunIds (separated by commas)",
            "diagnosticInputRequiredClients": "Portal",
            "required": true
        },
        {
            "id": "ir_type",
            "order": 6,
			"visibility": "null",
            "controlType": "dropdown",
            "displayLabel": "Which type of integration runtime are you using?",
            "watermarkText": "Choose an IR type",
            "dropdownOptions": [
                {
                    "value": "Azure IR",
                    "text": "Azure IR"
                },
                {
                    "value": "Self-hosted IR",
                    "text": "Self-hosted IR"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_report_id",
            "order": 7,
			"visibility": "ir_type == Self-hosted IR",
            "controlType": "textbox",
            "displayLabel": "Please provide the ReportIDs from all nodes separated with commas. (see Solutions tab for guidance on how to obtain the ReportID)",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
