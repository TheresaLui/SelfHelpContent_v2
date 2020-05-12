<properties
                pageTitle="servicewhitelistingsubscriptionissue"
                description="servicewhitelistingsubscriptionissue"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739971"
                productPesIds="17080"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="164b5696-324a-4397-b222-7fa69331c62b"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
            "title": "servicewhitelistingsubscriptionissue",
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
            "id": "ExpressRouteURIID",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the ExpressRoute URI ID of the private cloud?",
            "required": false
        }
            ]
 }
---
