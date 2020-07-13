<properties
                pageTitle="provisionprivatecloud"
                description="provisionprivatecloud"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739969"
                productPesIds="17080"
                cloudEnvironments="Public, fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="a9069eef-d6a3-4294-b0b8-66f55e28a781"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "provisionprivatecloud",
            "fileAttachmentHint": "",
            "formElements": [{
            			"id": "problem_start_time",
				"order": 1,
				"controlType": "datetimepicker",
				"displayLabel": "When did the problem begin?",
				"required": true
		}, {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message?",
            "required": true,
	    "useAsAdditionalDetails": true,
	    "hints": [{
					"text": "Provide details about the issue."
				}]
        },
        {
            "id": "CorrelationID",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the Correlation ID of the failed deployment?",
            "required": false
        },
        {
            "id": "Resourcename",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the Resource name?",
            "required": false
        },
        {
            "id": "ResourceGroup",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the Resource group?",
            "required": false
        }
            ]
 }
---
