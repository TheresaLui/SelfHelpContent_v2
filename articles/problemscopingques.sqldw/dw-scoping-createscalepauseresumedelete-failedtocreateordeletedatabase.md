<properties
	articleId="dw-scoping-createscalepauseresumedelete-failedtocreateordeletedatabase.md"
	pageTitle="Failed to create or delete database"
	description="Failed to create or delete database"
	authors="saltug,mlee3gsd"
	ms.author="saltug,martinle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635196"
	productPesIds="15818"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Create/Scale/Pause/Resume/Delete/Failed to create or delete database
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Failed to create or delete database",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "dw_scoping_crud_faileddatabase_portal",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Was the operation initiated through the portal?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_faileddatabase_programmatic",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "If the operation was programmatic using an ARM template, please provide the template.",
            "required": false
        },
        {
            "id": "dw_scoping_crud_faileddatabase_error",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "If an error was displayed, what was the error message?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_faileddatabase_create",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Is the failure during the create operation?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_faileddatabase_delete",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Is the failure during the delete operation?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
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