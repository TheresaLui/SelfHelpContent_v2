<properties
                pageTitle="accessservicesrunningintheprivatecloud"
                description="accessaccessservicesrunningintheprivatecloudvcenter"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739944"
                productPesIds="17080"
                cloudEnvironments="Public, fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="7824ec52-5a41-4072-8992-ef706c020819"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "accessservicesrunningintheprivatecloud",
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
            "id": "worked",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Has this worked previously?",
            "required": false
        }, {
            "id": "nsxt",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Has the T1 router and network segments been configured and firewall rules enabled in NSX-T?",
            "required": false
        }
            ]
 }
---
