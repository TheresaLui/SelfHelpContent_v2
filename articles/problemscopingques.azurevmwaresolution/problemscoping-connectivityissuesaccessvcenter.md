<properties
                pageTitle="accessvcenter"
                description="accessvcenter"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739945"
                productPesIds="17080"
                cloudEnvironments="Public, fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="aa262eb6-0471-4837-8af1-5ad376bfd698"
	              ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "accessvcenter",
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
            "displayLabel": "What is the error or warning message?",
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
