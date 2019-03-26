<properties
	articleId="dw-scoping-createscalepauseresumedelete-failedtocreateordeleteserver.md"
	pageTitle="Failed to create or delete server"
	description="Failed to create or delete server"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635197"
	productPesIds="15818"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Create/Scale/Pause/Resume/Delete/Failed to create or delete server
---
{
	"resourceRequired": true,
	"title": "Failed to create or delete server",
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
			"id": "dw_scoping_crud_failedserver_error",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "If an error was displayed, what was the error message?",
			"required": false
		}
		{
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
	]
}
---