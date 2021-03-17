<properties
                pageTitle="accessnxtmanager"
                description="accessnxtmanager"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739943"
                productPesIds="17080"
                cloudEnvironments="Public, fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="df02e57f-899c-42a3-80fc-c9b8628cd12d"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "accessnxtmanager",
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
					"text": "Provide the issue and error in detail."
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
            "id": "credentialissue",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Is this a credential issue?",
            "required": false
        }
            ]
 }
---
