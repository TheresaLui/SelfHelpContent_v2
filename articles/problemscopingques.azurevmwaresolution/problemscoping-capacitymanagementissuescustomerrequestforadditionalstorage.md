<properties
                pageTitle="customerrequestforadditionalstorage"
                description="customerrequestforadditionalstorage"
                ms.author="neshenoy"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32739954"
                productPesIds="17080"
                cloudEnvironments="Publicstorage
                schemaVersion="1"
                articleId="16d08774-9e09-4757-8230-43d2a9ee354f"
	            ownershipId="Azure_VMwareSolution_Content"
/>
# Useful Title
---
{
    "$schema": "Self Help Content",
    "subscription Required": true,
    "resource Required": false,
    "title": "customerrequestforadditionalstorage",
    "fileAttachmentHint": "",
    "formElements": [{
            			"id": "problem_start_time",
				"order": 1,
				"ControlType": "datetimepicker",
				"display Label": "When did the problem begin?",
				"Required": true
		}, {
            "id": "problem_description",
            "order": 2,
            "control Type": "multiline textbox",
            "displayLabel": "What is the error message?",
            "Required": true,
	    "useAsAdditionalDetails": true,
	    "hints": [{
					"text": "Provide details about the issue. N/A if not applicable."
				}]
        },
        {
            "id": "subscriptionID",
            "order": 3,
            "control Type": "textbox",
            "displayLabel": "What is the subscription ID?",
            "Required": false
        },
        {
            "id": "hosts required",
            "order": 4,
            "control Type": "textbox",
            "displayLabel": "How many more hosts are required?",
            "Required": false
        }
            ]
 }
---
