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
    "id" : "service_name",
                    "order" : 2,
                    "controlType" : "textbox",
                    "displayLabel" : "Webservice name",
                    "required": false
},
{
            "id" : "deployment_triggered",
                    "order" : 3,
                    "controlType" : "textbox",
                    "displayLabel" : "How was the deployment triggered (UI or SDK or CLI or direct REST Calls)?",
                    "required": false
        },
{
            "id" : "sdk_cli_version",
                    "order" : 4,
                    "controlType" : "textbox",
                    "displayLabel" : "If you deployed using SDK/CLI, what version?",
                    "required": false
        },
{
            "id": "problem_description",
			    "order": 5,
			    "controlType": "multilinetextbox",
			    "displayLabel": "Additional Details",
			    "watermarkText": "Please provide additional details, description of the issue",
			    "required": true,
			    "useAsAdditionalDetails": true,
			    "hints": [{
					"text": "Please upload service.get_logs()"
				}, {
					"text": "Please upload scoring script"
				},
                {
                     "text" : "Please upload screenshot of your error"
                }]
           }
    ]
}
---
