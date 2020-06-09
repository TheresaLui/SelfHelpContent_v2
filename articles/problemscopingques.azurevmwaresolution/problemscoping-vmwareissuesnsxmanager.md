<properties
                pageTitle="nsxmanager"
                description="nsxmanager"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739967"
                productPesIds="17080"
                cloudEnvironments="Public, fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="8fcf120d-5f5e-46ad-a9ee-3db49e1e5cd1"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "nsxmanager",
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
            "displayLabel": "What is nature of the issue?",
            "required": true,
	    "useAsAdditionalDetails": true,
	    "hints": [{
					"text": "Please describe the nature of the issue"
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