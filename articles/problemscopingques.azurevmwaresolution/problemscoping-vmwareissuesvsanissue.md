<properties
                pageTitle="vsanissue"
                description="vsanissue"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739978"
                productPesIds="17080"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="f2577a8a-d8c5-4f10-adef-5301359778ad"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
            "title": "vsanissue",
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
					"text": "What is nature of the issue?"
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
