<properties
	pageTitle="problemscopingques problem creating or running machine learning pipelines"
	description="Problem creating or running machine learning pipelines - scoping questions"
	service="microsoft.machinelearning"
	resource="machinelearning"
	ms.author="shbijlan"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690845,32690881,32690847,32690846"
	productPesIds="16644"
	cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="problemscopingques-machinelearning-pipelines"
	ownershipID="AzureML_AzureMachineLearningServices"
/>

# Problem creating or running machine learning pipelines: scoping questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem creating or running machine learning pipelines",
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
                "id": "problem_requestid",
                "order": 2,
                "controlType": "textbox",
                "displayLabel": "RequestId in the error message",
                "required": false
    },
          {
                "id": "problem_sdk_version",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "What version of SDK are you using?",
                "required": false
    },
          {
                "id": "problem_pipelinerunid",
                "order": 4,
                "controlType": "textbox",
                "displayLabel": "Please provide the runid(s) for failed/ troublesome runs",
                "required": false
	},
          {
                "id": "problem_pipelinerunurl",
                "order": 5,
                "controlType": "textbox",
                "displayLabel": "Please provide pipeline run/pipeline draft URL",
                "required": false
	},
		      {
                "id": "problem_description",
                "order": 6,
                "controlType": "multilinetextbox",
                "displayLabel": "Details",
                "watermarkText": "Provide detailed information about your issue",
                "required": true,
                "useAsAdditionalDetails": true,
                "hints": [{
                    "text": "Issue description"
                  }, {
                    "text": "Step Run ID (Find under *Details** tab in the module right pane)"
                  }, {
                    "text": "Detailed error message"
                  }, {
                    "text": "Attach all the logs under ‘Logs’ tab of said run id"
				          }
			]
		}
	]
}
---
