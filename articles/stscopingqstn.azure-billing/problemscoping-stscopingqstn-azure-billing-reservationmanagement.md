<properties
	pageTitle="Scoping questions for Reservation Management"
	description="Scoping questions for Reservation Management"
	authors="prdasneo"
   selfHelpType="problemScopingQuestions"
	supportTopicIds="32593226"
	productPesIds="15659"
	cloudEnvironments="public"
   schemaVersion="1"
   articleId="2c14140e-abca-4ef8-8c67-f5ebd7974567"
/>
# Reservation Management
Please provide the reservation type: <br>
---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Virtual machine - [Learn more about Azure RIs](https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances?toc=/azure/billing/TOC.json)"
                },
                {
                    "text": "SQL Database - [Learn more about SQL Reserved Instance](https://docs.microsoft.com/azure/sql-database/sql-database-reserved-capacity?toc=/azure/billing/TOC.json)"
                },
                {
                    "text": "SUSE Linux - [Learn more about SUSE Linux](https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges?toc=/azure/billing/TOC.json)"
                }
            ]
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ]
}
---