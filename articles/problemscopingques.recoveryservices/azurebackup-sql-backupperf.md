<properties
         pageTitle="Scoping questions for SQL database backup performance"
         description="Scoping questions for SQL database backup performance"
         authors="srinathv"
         ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32605792"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="18b06d30-478c-4950-b3bc-5ed2dfecdd7d"
/>
# Scoping questions for SQL database backup performance
---
{
    "resourceRequired": true,
    "title": "SQL database backup performance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "machine_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine running SQL",
            "required": true
        },{
            "id": "database_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the databases whose backup is slow?",
            "watermarkText": "Enter database name(s) comma separated",
            "required": true
        },
        {
            "id": "backup_Type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which type of performance issue are you facing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Slow backup during Full backup",
                    "text": "Slow backup during Full backup"
                },
                {
                    "value": "Slow backup during Log backup",
                    "text": "Slow backup during Log backup"
                },
                {
                    "value": "Slow backup during Differential backup",
                    "text": "Slow backup during Differential backup"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "jobID_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Enter the long running job activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
		{
            "id": "job_Running_Time",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Since how long the job is running?",
            "watermarkText": "Enter time in hours ex. 18hrs",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ]
}
---
