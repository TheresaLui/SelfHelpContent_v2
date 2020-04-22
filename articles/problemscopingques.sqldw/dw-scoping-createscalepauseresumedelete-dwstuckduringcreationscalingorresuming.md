<properties
    articleId="dw-scoping-createscalepauseresumedelete-dwstuckduringcreationscalingorresuming.md"
    pageTitle="Create/Scale/Pause/Resume/Delete database taking too long"
    description="Create/Scale/Pause/Resume/Delete database taking too long"
    authors="mlee3gsd"
    ms.author="martinle"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32635193, 32635192"
    productPesIds="15818"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>

# Create, Scale, Pause, Resume, Delete - Create, Scale, Pause, Resume or Delete database taking too long

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Region unavailable for Data Warehouse creation",
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
            "id": "dw_scoping_crud_operation_create",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Are you experiencing this during the create operation?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_operation_scale",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Are you experiencing this during the scale operation?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_operation_resume",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Are you experiencing this during the resume operation?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_operation_howlong",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "How long has this operation have been running?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_operation_error",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "If an error was displayed, what was the error message?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_operation_region",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What region is your data warehouse?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
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
