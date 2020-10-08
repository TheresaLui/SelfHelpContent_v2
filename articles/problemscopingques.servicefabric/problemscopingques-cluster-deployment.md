<properties
	pageTitle="Cluster Deployment"
	description="Cluster Deployment"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32690994"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-cluster-deployment"
	ownershipId="Compute_ServiceFabric"
/>
# Cluster Deployment
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ARM Templates",
    "fileAttachmentHint": "Please attach the ARM template used to deploy the cluster as well as any relevant logs/screenshots.",
    "formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
		{
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		},
        {
            "id": "keyvault_region",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel":  "Is the Azure Key Vault where your certificate is stored located in the same region as your cluster?",
            "watermarkText":  "Choose an option",
            "dropdownOptions": [{
                "value": "Yes",
                "text": "Yes"
            },{
                "value": "No",
                "text": "No"
            }],
            "required": false
        }
	],
    "$schema": "SelfHelpContent"
}
---