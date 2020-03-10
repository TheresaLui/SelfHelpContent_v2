<properties pageTitle="Cannot connect to SQL Server"
	 description="Cannot connect to SQL Server"
	 authors="yareyes"
	 ms.author="yareyes"
	 selfHelpType="problemScopingQuestions"
	 supportTopicIds="32639651,32639652,32639650"
	 productPesIds="14745"
	 cloudEnvironments="public,fairfax"
	 schemaVersion="1"
	 articleId="036d4c3f-d462-4c80-a716-fdf69dfdda6a"
	ownershipId="AzureData_AzureSQLVM"
/>
# Cannot connect to SQL Server
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cannot connect to SQL Server",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "connectivity_problem",
            "visibility": null,
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": " Is the connectivity constant or intermittent?",
            "watermarkText": "Choose an option",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Consistent (every time I try to connect)",
                    "value": "Consistent"
                },
                {
                    "text": "Intermittent (sometimes connections work)",
                    "value": "Intermittent"
                },
                {
                    "text": "I’m not sure/don’t know",
                    "value": "dont_know_answer"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "error_message",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Which error message are you encountering?",
            "watermarkText": "Provide the error message",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "source_of_connection",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the source of the connection?",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Locally, on the database server",
                    "value": "Local"
                },
                {
                    "text": "Another virtual machine in the same Azure VNET",
                    "value": "AnotherVmSameVnet"
                },
                {
                    "text": "Another virtual machine in Azure",
                    "value": "AnotherVmDiffVnet"
                },
                {
                    "text": "An Azure Web App",
                    "value": "AzureWebApp"
                },
                {
                    "text": "An on-premises workstation or server",
                    "value": "OnPremiseServer"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "destination_of_connection",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What is the destination of the connection?",
            "content": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "An Azure Virtual Machine with SQL Server installed (IaaS)",
                    "value": "AzureVm"
                },
                {
                    "text": "Azure SQL Database (PaaS)",
                    "value": "AzureSqlDb"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
