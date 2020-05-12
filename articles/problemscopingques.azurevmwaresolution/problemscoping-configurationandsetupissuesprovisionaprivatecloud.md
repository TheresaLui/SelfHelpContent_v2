<properties
                pageTitle="provisionaprivatecloud"
                description="provisionaprivatecloud"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739969"
                productPesIds="17080"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="c8d19aa7-ad4a-4fa1-811b-b3048d3c4c24"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
            "title": "provisionaprivatecloud",
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
					"text": "What is the error message?"
				}]
        },
        {
            "id": "CorrelationID",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the Correlation ID of the failed deployment?",
            "required": false
        }
        ,
        {
            "id": "ResourceID",
            "order": 4
            "controlType": "textbox",
            "displayLabel": "What is the Resource ID?",
            "required": false
        }
        ,
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
