<properties
                pageTitle="tenantvnetresources"
                description="tenantvnetresources"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739942"
                productPesIds="17080"
                cloudEnvironments="Public, fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="2e134af6-2175-4e8b-b855-08e475e7b915"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "tenantvnetresources",
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
            "displayLabel": "What is error message?",
            "required": true,
	    "useAsAdditionalDetails": true,
	    "hints": [{
					"text": "Provide the issue and error in detail"
				}]
        },
        {
            "id": "expressrouteid",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the ExpressRoute URI ID?",
            "required": false
        },
        {
            "id": "ergateway",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Is the ER gateway in the Vnet peered with private cloud ExpressRoute circuit?",
            "required": false
        }
            ]
 }
---
