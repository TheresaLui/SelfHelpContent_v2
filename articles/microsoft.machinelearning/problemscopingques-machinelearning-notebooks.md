<properties
	pageTitle="problemscopingquestions-notebooks"
	description="Notebooks - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739643,32739644,32739647,32739649,32739650,32739651,32739648,32739645,32739646"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingquestions-machinelearning-notebooks"
	ownershipId="AzureML_AzureMachineLearningServices"
/>


# Notebooks - scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Notebooks - scoping questions",
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
			"id": "problem_networking",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What are your networking configurations / What firewalls do you have applied?",
			"required": false
	},
			{
			"id": "problem_permissions",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What permissions do you have (owner, contributor, or custom role)? For custom roles, list all actions you have enabled",
			"required": false
	},
  {
			"id": "problem_errormessagedetails",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the error message and correlation ID?",
			"required": true
	},
		{
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Issue description."
				}
			]
		}
	]
}
---
