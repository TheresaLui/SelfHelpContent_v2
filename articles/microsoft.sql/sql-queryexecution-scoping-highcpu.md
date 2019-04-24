<properties
	pageTitle="Scoping questions for Unexpected increase in resource consumption or DTUs"
	description="Unexpected increase in resource consumption or DTUs"
	service="microsoft.sql"
	authors="pxding"
        ms.author="pedin"
        articleId="5CD44772-DC30-406B-9E16-9FCBFBB5452F"
        selfHelpType="ProblemScopingQuestions"
        supportTopicIds="32630459"
        productPesIds="13491"
	cloudEnvironments="public"
        schemaVersion="1"
/>

# Unexpected increase in resource consumption or DTUs

---
{
    "resourceRequired": true,
    "title": "Unexpected increase in resource consumption or DTUs",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What is the start time of the issue?",
            "required": true
        },{
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "What is the end time of the issue?",
            "required": true
        },{
	    "id": "feature_dropdown",
	    "order": 3,
	    "controlType": "dropdown",
	    "displayLabel": "Which rsource consumption increase are you requesting help for?",
	    "watermarkText": "Choose an option",
	    "dropdownOptions": [{
		"value": "CPU_consumption_increased",
		"text": "CPU consumption increased"
		}, {
		"value": "IO_consumption_increased",
		"text": "IO consumption increased"
		}, {
		"value": "Memory_consumption_increased",
		"text": "Memory consumption increased"
		}, {
		"value": "Increase_Other",
		"text": "Other resource consumption increase not listed"
                }, {
		"value": "dont_know_answer",
		"text": "Don't know answer"
		}
		],
		"required": true
        },{
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Details of the issue.",
            "watermarkText": "Provide additional information about your unexpected increase in resource consumption or DTUs.",
            "required": true
        }
    ]
}
---



