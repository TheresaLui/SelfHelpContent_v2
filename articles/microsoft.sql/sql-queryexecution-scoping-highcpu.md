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
            "id": "perf_cpu_detect",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "How did you detect high CPU usage?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Perf Insights",
                    "text": "Perf Insights"
                },
                {
                    "value": "Azure Monitoring Alerts",
                    "text": "Azure Monitoring Alerts"
                },
                {
                    "value": "Other Monitoring tools (describe below)",
                    "text": "Other Monitoring tools (describe below)"
                }
            ],
            "required": false
         }
    ]
}

---



