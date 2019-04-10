<properties
	articleId="dw-scoping-performanceandqueryexecution.md"
	pageTitle="Performance and Query Execution"
	description="Performance and Query Execution"
	authors="saltug,happynicolle"
	ms.author="saltug,nicw"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635180, 32635210, 32635214, 32635219"
	productPesIds="15818"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Performance and Query Execution
---
{
	"resourceRequired": true,
	"title": "Performance and Query Execution",
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
			"id": "dw_scoping_perf_queryid",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "If a query is involved, what is the query id?",
			"required": false
		},
		{
			"id": "dw_scoping_perf_error",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "If an error was displayed, what was the error message?",
			"required": false
		},
		{
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
	]
}
---