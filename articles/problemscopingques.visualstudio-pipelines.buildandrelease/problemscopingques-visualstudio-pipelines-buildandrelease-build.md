<properties
	pageTitle="Scoping questions for Pipelines Build Issues"
	description="Scoping questions for Pipelines Build Issues"
	authors="chrisjco"
	ms.author="ccoop"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32452973, 32452974, 32572374, 32572376"
	productPesIds="15543"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-visualstudio-pipelines-buildandrelease-build"
/>
# Pipelines Issues - Build
---
{
	"resourceRequired": false,
	"title": Pipeline Issues",
	"subscriptionRequired": false,
	"fileAttachmentHint": "Upload any screenshots or log files of the error or issue",
	"formElements": [
		{	
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Problem start time",
			"required": true
		}, 
		{	"id": "org_name",
			"order": 2,
			"controlType": "textbox",
        	"displayLabel": "Please provide your Azure DevOps Organization name (like XYZ.visualstudio.com \ dev.azure.com/XYZ)",
            "required": true
		},
		{	"id": "project_name",
			"order": 3,
			"controlType": "textbox",
          	"displayLabel": "Name of project affected",
           	"required": true
		},
		{	"id": "definition_name",
			"order": 4,
			"controlType": "textbox",
            "displayLabel": "Name of definition affected",
            "required": true
		},
		{
            "id": "problem_description",
        	"order": 5,
          	"controlType": "multilinetextbox",
       		"displayLabel": "Please provide these details",
       		"required": true,
        	"watermarkText": "Please provide: a detailed scenario of the error condition or issue, troubleshooting done so far, and any other relevant information.",
        	"useAsAdditionalDetails": true,
           		"hints": 
			[
                {
                    	"text": "Expected behavior, actual behavior"
                },
                {
                    	"text": "Troubleshooting done so far"
                },
                {
						"text":  "Additional details"
				},
				{
                    	"text": "Screenshots"
                }
            ]
        }
	]
}
---