<properties
                pageTitle="vcenterother"
                description="vcenterother"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739974"
                productPesIds="17080"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="65c786bf-fde0-4a9b-895e-65119ce61119"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
            "title": "vcenterother",
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
        }            ]
 }
---
