<properties
	pageTitle="Application POA"
	description="Application POA"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32690998"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-application-poa"
	ownershipId="Compute_ServiceFabric"
/>
# Application Upgrade
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Application Upgrade",
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
            "id": "failure_reason",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Upgrade Failure",
            "watermarkText": "Using the cmdlet Get-ServiceFabricApplicationUpgrade do you see any FailureReason or any safety checks in the UpgradeDomainProgressAtFailure?",
            "required": false
        }
	],
    "$schema": "SelfHelpContent"
}
---