<properties
    pageTitle="problemscopingques machinelearning model deployment"
    description= "scoping questions for consuming web service and data collection"
    authors="shivanissambare"
    ms.author= "ssambare"
    selfHelpType="problemScopingQuestions"
    supportTopicIds= "32690850, 32690875"
    productPesIds= "16644"
    articleId= "problemscopingques-model deployment"
    cloudEnvironments= "public,fairfax,mooncake,usnat,ussec"
    schemaVersion= "1"
    ownershipID="AzureML_AzureMachineLearningServices"
/>

# Problem with consuming web service and model data collection : scoping questions
---

{
 "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem with consuming web service and model data collection",
    "fileAttachmentHint": "",
    "formElements":
    [
 {
            "id": "problem_start_time",
            		"order": 1,
            		"controlType": "datetimepicker",
            		"displayLabel": "When did the problem start?",
            		"required": true
        },
{
            "id": "problem_description",
			    "order": 2,
			    "controlType": "multilinetextbox",
			    "displayLabel": "Attachment",
			    "watermarkText": "Please provide additional details you think are important",
			    "required": true,
			    "useAsAdditionalDetails": true,
			    "hints": [{
					"text": "Please attach `service.get_logs()`"
				}, {
					"text": "Please attach scoring script"
				},
                {
                     "text" : "Please attach screenshot of your error"
                }]
           }
    ]
}
---
