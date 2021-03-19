<properties
	pageTitle="Cluster Upgrade Stuck"
	description="Cluster Upgrade Stuck"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32690995, 32690989"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-cluster-upgrade-stuck"
	ownershipId="Compute_ServiceFabric"
/>
# Cluster Upgrade Stuck
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cluster Upgrade Stuck",
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
			"id": "application_errors",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Were any applications in error state when the cluster upgrade started? If so, please provide the names of the applications.",
			"required": false
		}
	],
    "$schema": "SelfHelpContent"
}
---