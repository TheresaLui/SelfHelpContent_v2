<properties
	pageTitle="problemscopingquestions studio (classic)"
	description="Studio (classic) - scoping questions"
	service="microsoft.machinelearningstudioclassic"
	resource="machinelearning"
	authors="SturgeonMi"
	ms.author="keli19"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32321860,32321848,32321850,32321867,32321847,32321856,32355159,32355170,32321879"
	productPesIds="15570"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingques-machinelearning-studioclassic"
	ownershipID="AzureML_AzureMachineLearning"
/>

# Problem with Studio (classic): scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem with Studio (classic)",
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
			"id": "problem_experiment_url",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What is the URL of your experiment?",
			"required": false
	},
		{
			"id": "problem_webservice",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What is the URL of your web service?",
			"required": false
	},
		{
			"id": "problem_description",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide detailed information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description"
				},{
					"text": "Detailed error message"
				}
			]
		}
	]
}
---

