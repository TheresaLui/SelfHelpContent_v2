<properties
                pageTitle="customerrequestforadditionalbandwidthcapacity"
                description="customerrequestforadditionalbandwidthcapacity"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739953"
                productPesIds="17080"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="9fbe02da-8a04-41ef-ae4c-33c13f0418d0"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "customerrequestforadditionalbandwidthcapacity",
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
            "displayLabel": "What is the reason more capacity is needed?",
            "required": true,
	    "useAsAdditionalDetails": true,
	    "hints": [{
					"text": "Provide the reason why more capacity is needed"
				}]
        },
        {
            "id": "ExpressRouteID",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the ExpressRoute ID of the private cloud?",
            "required": false
        }
            ]
 }
---
