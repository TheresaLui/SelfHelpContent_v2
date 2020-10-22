<properties
    pageTitle="problemscopingques machinelearning deployment"
    description= "scoping questions for model deployment and serving"
    authors="shivanissambare"
    ms.author= "ssambare"
    selfHelpType="problemScopingQuestions"
    supportTopicIds= "32690852"
    productPesIds= "16644"
    articleId= "problemscopingques-model deployment and serving"
    cloudEnvironments= "public,fairfax,mooncake,usnat,ussec"
    schemaVersion= "1"
    ownershipID="AzureML_AzureMachineLearningServices"
/>

# Problem with model deployment and serving : scoping questions
---
{
 "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem with Model Deployment and Serving",
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
            "id" : "workspace_behind_vnet"
                    "order" : 2,
                    "contorlType" : "textbox"
                    "displayLabel" : "Are the workspace resources (storage, ACR) behind VNet?",
                    "required": false
        },
        {
            "id" : "privatelink_workspace"
                    "order" : 3,
                    "contorlType" : "textbox"
                    "displayLabel" : "Is it a private linked workspace?"
                    "required": false
        },
       {
            "id" : "deployment_triggered"
                    "order" : 4,
                    "contorlType" : "textbox"
                    "displayLabel" : "Was the deployment triggered via UI or SDK or CLI or direct REST Calls?",
                    "required": false
        },
       {
            "id" : "gpu_deployment"
                    "order" : 5,
                    "contorlType" : "textbox"
                    "displayLabel" : "Are you trying to do GPU based deployment",
                    "required": false
        },
       {
            "id" : "working_before_deployment"
                    "order" : 6,
                    "contorlType" : "textbox"
                    "displayLabel" : "Were these deployments working before and now have started to fail?",
                    "required": false
        },
       {
            "id" : "frequency_deployment_working_before"
                    "order" : 7,
                    "contorlType" : "textbox"
                    "displayLabel" : "Are the deployments failing 100% of the times or failure is transient?",
                    "required": false
        },
       {
            "id" : "service_name_with_failed_deployment"
                    "order" : 8,
                    "contorlType" : "textbox"
                    "displayLabel" : "Service name with failed deployment",
                    "required": false
        },
       {
            "id" : "aci_deployment_question"
                    "order" : 9,
                    "contorlType" : "textbox"
                    "displayLabel" : "For ACI Deployment only, Please go to your workspace resource group, click on ACI resource (name is same as the service name), What is the status of the overall ACI? (Attach screenshot if possible)",
                    "required": false
        },
       {
            "id" : "aks_deployment_question1"
                    "order" : 10,
                    "contorlType" : "textbox"
                    "displayLabel" : "For AKS deployments only, does the cluster have internal load balancer setup?",
                    "required": false
        },
       {
            "id" : "aks_deployment_question2"
                    "order" : 11,
                    "contorlType" : "textbox"
                    "displayLabel" : "For AKS deployments only, is the cluster set up with AutoSSL?",
                    "required": false
        },
       {
            "id" : "model_question"
                    "order" : 12,
                    "contorlType" : "textbox"
                    "displayLabel" : "Model Size",
                    "required": false
        },
        {
            "id" : "sdk_cli_version"
                    "order" : 13,
                    "contorlType" : "textbox"
                    "displayLabel" : "If you deployed using SDK/CLI, what version?",
                    "required": false
        },
        {
            "id": "problem_description",
			    "order": 14,
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