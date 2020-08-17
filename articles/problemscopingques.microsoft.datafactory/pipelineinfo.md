<properties
	pageTitle="Azure Data Factory Pipeline Info"
	description="Scoping questions to gather Azure Data Factory pipeline information"
	authors="lisaliu,hecepeda"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629483,32637158,32637159,32629480,32629495,32637161,32740731"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="BE3D6801-3F87-41BC-ACF9-B9DA8A86C55C"
	ownershipId="AzureData_DataFactory"
/>
# Azure Data Factory Pipeline Info
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Factory Pipeline Info",
    "fileAttachmentHint": "Please attach JSON code for dataset, linked service, and output of activity run to help us triage your problem faster",
    "diagnosticCard": {
        "title": "Azure Pipeline Activity Troubleshooter",
        "description": "Our Pipeline Activity RunId Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect the issues we were looking for in your resource. Refer to the help manual below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
			"diagnosticInputRequiredClients": "Portal",
            "required": true
        },
        {
            "id": "problem_run_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Is this a run time issue? If yes, Provide the Pipeline or Activity RunIds (separated by commas)",
			"diagnosticInputRequiredClients": "Portal",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Exact error message if applicable"
                },
                {
                    "text": "Is the issue intermittent or persistent?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
