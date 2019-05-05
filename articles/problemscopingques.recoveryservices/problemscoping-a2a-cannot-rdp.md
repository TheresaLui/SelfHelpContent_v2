<properties
                pageTitle="Scoping questions for Site Recovery (Azure to Azure)/Unable to connect"
                description="Cannot Connect to My Virtual Machine after failover"
                authors="genlin"
                ms.author="asgang"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32574725"
                productPesIds="16370"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="47777774-20f7-4eba-8b3e-7fb11cc74cf2"
/>
# Connect to a VM
---
{
    "resourceRequired": true,
    "title": "Failure to connect to the RDP port",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "connect_error",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error you received?",
            "required": false
        },
        {
            "id": "vm_facing_issue",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": true
        },
        {
            "id": "ippublicprivate",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Do you have issues connecting the VM by using public or private IP?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Public IP",
                    "text": "Public IP"
                },
                {
                    "value": "Private IP",
                    "text": "Private IP"
                }
            ],
            "required": false
        },
        {
            "id": "ippublic",
            "order": 4,
            "visibility": "ippublicprivate == Public IP",
            "controlType": "dropdown",
            "displayLabel": "Are you able to connect to the Private IP?",
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
        },
        {
            "id": "ipprivate",
            "order": 5,
            "visibility": "ippublicprivate == Private IP",
            "controlType": "dropdown",
            "displayLabel": "Are you able to connect to the Public IP?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "I don't have a Public IP",
                    "text": "I don't have a Public IP"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        }
    ]
}
---
