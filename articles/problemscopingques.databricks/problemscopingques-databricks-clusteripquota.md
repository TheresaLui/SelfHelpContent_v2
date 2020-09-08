<properties
	articleId="21061cae-3950-4bbf-a216-2e31a8357224"
	pageTitle="Scoping Questions for Databricks Cluster Create failure involving library"
	description="Scoping Questions for Databricks Cluster Create failure involving library"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743377"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Creation Termination Sizing Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Databricks Cluster Creationg Termination Sizing Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "errormessage",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message you received?",
            "watermarkText": "Please copy paste the full error text including the stack trace if available",
            "required": false
        },
        {
            "id": "corelimit",
            "order": 40,
            "controlType": "textbox",
            "displayLabel": "What is the IP quota limit set for this subscription?",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "cluster_url",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Cluster URL if available",
            "infoBalloonText": "Follow this <a href='https://docs.azuredatabricks.net/user-guide/faq/workspace-details.html'>article</a> to get Cluster URL",
            "required": true
        },
        {
            "id": "workspace_id",
            "order": 170,
            "controlType": "textbox",
            "displayLabel": "Workspace ID if cluster URL is not available",
            "infoBalloonText": "Follow this <a href='https://docs.azuredatabricks.net/user-guide/faq/workspace-details.html'>article</a> to get Workspace ID",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide any additional related to this issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
