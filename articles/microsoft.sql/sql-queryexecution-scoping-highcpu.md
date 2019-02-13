<properties
	pageTitle="Scoping questions for SQL DB high CPU usage"
	description="High CPU usage"
	service="microsoft.sql"
	authors="pxding"
        ms.author="pedin"
        articleId="5CD44772-DC30-406B-9E16-9FCBFBB5452F"
        selfHelpType="ProblemScopingQuestions"
        supportTopicIds="32630450"
        productPesIds="13491"
	cloudEnvironments="public"
        schemaVersion="1"
/>

# High CPU usage

---
{
    "resourceRequired": true,
    "title": "CPU is higher than expected",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What is the start time of the issue?",
            "required": true
        },{
            "id": "perf_current",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is the high CPU issue ongoing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],

            "required": false
        },{
            "id": "perf_benchmarking",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your high CPU issue",
            "required": true,
            "hints": [
                {
                    "text": "How much CPU resourece consumption are you seeing"
                },
                {
                    "text": "Has the site volume increased"
                }
            ]
        }
    ]
}

---



