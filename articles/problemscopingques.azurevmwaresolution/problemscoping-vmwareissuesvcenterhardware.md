<properties
                pageTitle="vcenterhardware"
                description="vcenterhardware"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739974"
                productPesIds="17080"
                cloudEnvironments="Public, fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="65c786bf-fde0-4a9b-895e-65119ce61119"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "vcenterhardware",
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
            "displayLabel": "What is the error or warning message reported in vCenter?",
            "required": true,
	    "useAsAdditionalDetails": true,
	    "hints": [{
					"text": "Provide details about the issue."
				}]
        },
        {
            "id": "ExpressRouteURIID",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the ExpressRoute URI ID of the private cloud?",
            "required": false
        }, {
            "id": "Cluster",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Which cluster is experiencing the issue?",
            "required": false
        }, {
            "id": "Host",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Which host in the cluster is reporting the issue?",
            "required": false
        }
            ]
 }
---
