<properties
	pageTitle="problemscopingques problem accessing studio"
	description="Problem accessing studio - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="tzvikei"
	ms.author="tzvikei"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740866,32740867"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingques-machinelearning-studio"
	ownershipID="AzureML_AzureMachineLearningServices"
/>

# Problem accessing Azure Machine Learning studio: scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem accessing studio",
    "fileAttachmentHint": "",
    "formElements":
    [
    	{
            	"id": "problem_start_time",
            	"order": 1,
            	"controlType": "datetimepicker",
            	"displayLabel": "When did the problem start?",
            	"required": false
    	},
    	{
		"id": "problem_scope",
		"order": 2,
		"controlType": "textbox",
		"displayLabel": "Which asset are you having issues accessing?",
		"required": true
	},
	{
		"id": "problem_description",
		"order": 3,
		"controlType": "multilinetextbox",
		"displayLabel": "What is the scope of the problem?",
		"watermarkText": "Does the problem concern logging in to studio, or does it concern accessing specific assets?",
		"required": true,
		"useAsAdditionalDetails": true,
		"hints": [{
				"text": "Can't get past the login or welcome page?"
			}, {
				"text": "Getting error for every page you are trying to load?"
			}, {
				"text": "Can't find or access specific assets like Datasets or Models?"
			}
		]
	}
	]
}
---
