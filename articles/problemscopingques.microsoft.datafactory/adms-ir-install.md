<properties
	pageTitle="Azure Data Movement IR installation info"
	description="Scoping questions to gather Azure Data Movement IR installation information"
	authors="hecepeda"
	ms.author="hecepeda"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32629536, 32629541"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="adms-ir-install.md"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Movement Integration Runtime Installation Issue

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Movement IR issue",
    "fileAttachmentHint": "Please attach JSON code for dataset, linked service and screen shots to help us triage your problem faster",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please briefly describe the issue",
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
            "id": "ir_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Name of the Self-Hosted IR",
            "required": false
        },
        {
            "id": "problem_report_id",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Is this a run time issue? If yes, please provide the Report ID. (see Solutions tab for guidance on how to obtain it)",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
