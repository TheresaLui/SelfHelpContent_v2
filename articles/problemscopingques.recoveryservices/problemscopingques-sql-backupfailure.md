<properties
         pageTitle="Scoping questions for SQL database backup failure"
         description="Scoping questions for SQL database backup failure"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32605791"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="d73dbe86-4f8e-414d-8963-7d22d012b671"
/>
# Questions SQL database backup failure
---
{
    "resourceRequired": true,
    "title": "SQL database backup failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "machine_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine running SQL",
            "required": true
        },
        {
            "id": "os_version",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the machine?",
            "watermarkText": "ex. Windows Server 2012 R2",
            "required": true
        },
        {
            "id": "sql_version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the SQL Server version and edition?",
            "watermarkText": "ex. SQL Server 2012 Standard",
            "required": true
        },
        {
            "id": "database_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the databases whose backup is failing?",
            "watermarkText": "Enter database name(s) comma separated",
            "required": true
        },
        {
            "id": "backup_Type",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the failure happening during Full/Log/Differential backup?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Full backup",
                    "text": "Full backup"
                },
                {
                    "value": "Log backup",
                    "text": "Log backup"
                },
                {
                    "value": "Differential backup",
                    "text": "Differential backup"
                }
            ],
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Enter the failed backup job Activity ID",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": true
        },
        {
            "id": "learn_more_text",
            "order": 7,
            "controlType": "infoblock",
            "content": "Microsoft can provide a solution to your problem faster if you can provide a failed Backup Job Activity ID. From a new browser tab, you can find this from Recovery Services Vault > Monitoring and Report > Backup Jobs > Failed > Activity ID."
        },
        {
            "id": "error_message",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste the error message details",
            "required": true
        },
        {
            "id": "prerequisites_links",
            "order": 9,
            "controlType": "infoblock",
            "content": "Ensure you review these prerequisites and dependencies for successful configuration and backup:, <a href='https://docs.microsoft.com/azure/backup/backup-azure-sql-database#supported-operating-systems'>supported OS version</a>, <a href='https://docs.microsoft.com/azure/backup/backup-azure-sql-database#supported-sql-server-versions-and-editions'>supported SQL server versions and editions</a>, <a href='https://docs.microsoft.com/azure/backup/backup-azure-sql-database#prerequisites'>permission required on VM.</a>"
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 10,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "OS version is supported for backup",
                    "text": "OS version is supported for backup"
                },
                {
                    "value": "SQL version and edition are supported for backup",
                    "text": "SQL version and edition are supported for backup"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "SQL server VM has required permission for backup",
                    "text": "SQL server VM has required permission for backup"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_date",
            "order": 11,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": false
        },
        {
            "id": "learn_more_text1",
            "order": 12,
            "controlType": "infoblock",
            "content": "Please upload SQL Server logs located at %ProgramFiles%\\Microsoft SQL Server\\MSSQL11.MSSQLSERVER\\MSSQL\\Log. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left."
        },
        {
            "id": "problem_description",
            "order": 13,
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
