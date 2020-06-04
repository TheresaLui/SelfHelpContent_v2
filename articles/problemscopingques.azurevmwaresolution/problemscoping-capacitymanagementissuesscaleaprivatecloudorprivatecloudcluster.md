<properties
                pageTitle="capacitymanagementissuesscaleaprivatecloudorprivatecloudcluster"
                description="capacitymanagementissuesscaleaprivatecloudorprivatecloudcluster"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739970"
                productPesIds="17080"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="4741f8a8-2340-4f37-9b00-f79762b01f8d"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "capacitymanagementissuesscaleaprivatecloudorprivatecloudcluster",
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
    "id": "Adding_a_cluster",
    "order": 3,
    "controlType": "multiselectdropdown",
    "displayLabel": "Are you adding a cluster to a private cloud or scaling an existing cluster?",
    "dropdownOptions": [{
            "value": "Adding a cluster",
            "text": "Adding a cluster"
        }, {
            "value": "Scaling an existing cluster",
            "text": "Scaling an existing cluster"
        }
    ],
    "required": false
},
       {
            "id": "CorrelationID",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the Correlation ID of the failed deployment?",
            "required": false
        },
        {
            "id": "ExpressRouteURIID",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the ExpressRoute URI ID?",
            "required": false
        },
        {
            "id": "Resourcename",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is the Resource name?",
            "required": false
        },
        {
            "id": "Resourcegroup",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What is the Resource group?",
            "required": false
        }]
 }
---
