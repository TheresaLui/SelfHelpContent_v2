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
---
{
    "resourceRequired": false,
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Virtual machine - <a href='https://docs.microsoft.com/azure/virtual-machines/windows/prepay-reserved-vm-instances?toc=/azure/billing/TOC.json'>Learn more about Azure RIs</a>"
                },
                {
                    "text": "SQL Database - <a href='https://docs.microsoft.com/azure/sql-database/sql-database-reserved-capacity?toc=/azure/billing/TOC.json'>Learn more about SQL Reserved Instance</a>"
                },
                {
                    "text": "SUSE Linux - <a href='https://docs.microsoft.com/azure/virtual-machines/linux/prepay-suse-software-charges?toc=/azure/billing/TOC.json'>Learn more about SUSE Linux</a>"
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