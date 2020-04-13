<properties
	articleId="dw-scoping-createscalepauseresumedelete-cannotscalehigherorlower.md"
	pageTitle="Cannot scale higher or lower"
	description="Cannot scale higher or lower"
	authors="saltug,mlee3gsd"
	ms.author="saltug,martinle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635190"
	productPesIds="15818"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_SQLDataWarehouse"
/>
# Create/Scale/Pause/Resume/Delete/Cannot scale higher or lower
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cannot scale higher or lower",
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
            "id": "dw_scoping_crud_cannotscale_portal",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Was the operation initiated through the portal?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_cannotscale_programmatic",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Was the operation initiated programmatically?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_cannotscale_region",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the region of your data warehouse?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_cannotscale_slo",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What performance tier are you requesting?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_cannotscale_error",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "If the operation failed, what is the error message that was displayed?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_cannotscale_quota",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What's your current DTU quota?",
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
