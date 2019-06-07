<properties
	articleId="dw-scoping-createscalepauseresumedelete-cannotscalehigherorlower.md"
	pageTitle="Cannot scale higher or lower"
	description="Cannot scale higher or lower"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635190"
	productPesIds="15818"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Create/Scale/Pause/Resume/Delete/Cannot scale higher or lower
---
{
    "resourceRequired": true,
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
            "id": "dw_scoping_crud_cannotscale_slo",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What service level are you trying to scale to?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_cannotscale_region",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What region are you trying to scale in?",
            "required": false
        },
        {
            "id": "dw_scoping_crud_cannotscale_quota",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's your current DTU quota?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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