<properties
                pageTitle="customerrequestforadditionalhostquotacapacity"
                description="customerrequestforadditionalhostquotacapacity"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739955"
                productPesIds="17080"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="7fe6817b-3791-42a1-a335-2fa1de591eb1"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
            "title": "customerrequestforadditionalhostquotacapacity",
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
					"text": "Provide details about the issue. N/A if not applicable"
				}]
        },
        {
            "id": "subscriptionID",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the subscription ID?",
            "required": false
        },
        {
            "id": "hostsrequired",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "How many more hosts are required?",
            "required": false
        }
            ]
 }
---
