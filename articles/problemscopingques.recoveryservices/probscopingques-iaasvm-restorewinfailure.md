<properties
         pageTitle="Scoping questions for Azure VM Restore failure for Windows"
         description="Scoping questions for Azure VM Restore failure for Windows"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553299"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	articleId="dcc0ea6d-9270-4719-82d0-a395117abb9f"
/>
# Questions Azure VM Restore failure for Windows 
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure VM Restore failure for Windows",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "using_VM",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": false
        },
        {
            "id": "JobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed restore job activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Restoration_Type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which type of restore you are performing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "Value": "Restoring VMs in Azure Portal",
                    "Text": "Restoring VMs in Azure Portal"
                },
                {
                    "Value": "Recovering files from Azure VMs backups",
                    "Text": "Recovering files from Azure VMs backups"
                },
                {
                    "Value": "Restore encrypted VMs",
                    "Text": "Restore encrypted VMs"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ]
}
---
