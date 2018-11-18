<properties
         pageTitle="Scoping questions for Azure VM backup or restore performance"
         description="Scoping questions for Azure VM backup or restore performance"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32565496"
         productPesIds="14749"
         cloudEnvironments="public"
         schemaVersion="1"
/>
# Questions Azure VM backup or restore performance
---
{
    "resourceRequired": true,
    "title": "Azure VM backup or restore performance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "using_VM",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine(s) is experiencing problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": true
        },
        {
            "id": "Issue_Type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which type of performance issue you are facing",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Slow backup during initial (first) backup",
                    "text": "Slow backup during initial (first) backup"
                },
                {
                    "value": "Slow backup during incremental backup",
                    "text": "Slow backup during incremental backup"
                },
                {
                    "value": "Slow restore",
                    "text": "Slow restore"
                }
            ],
            "required": true
        },
        {
            "id": "JobID_Name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Enter the long running job activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": true
        },
        {
            "id": "learn_more_text",
            "order": 4,
            "controlType": "infoblock",
            "content": "Microsoft can provide a solution to your problem faster if you can provide the long running Job Activity ID. From a new browser tab, You can find this from Recovery Services Vault > Monitoring and Report > Backup Jobs > Failed > Activity ID."
        },
        {
            "id": "job_Running_Time",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Since how long the job is running?",
            "watermarkText": "Enter time in hours ex. 18hrs",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ]
}
---
