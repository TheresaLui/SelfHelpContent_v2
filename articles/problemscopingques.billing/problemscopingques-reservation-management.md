<properties
	pageTitle="Reservation Management"
	description="Reservation Management"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32593227,32593228,32593229"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="b4b6273d-558e-4f2d-ab00-36a830ea4353"
/>


# RESERVATION MANAGEMENT
---
{
    "resourceRequired": false,
    "title": "Reservation Management",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "reservation_instance_determination",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Choose the type of Reservation Instance",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Virtual Instance",
                    "text": "Virtual Instance"
                },
                {
                    "value": "SQL database",
                    "text": "SQL database"
                },
                {
                    "value": "SUSE Software",
                    "text": "SUSE Software"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Type of Reservation : SUSE Linux, SQL Database, Virtual Machines RI"
                },
                {
                    "text": "Note: To ensure we capture all of your reservation details accurately, please raise a service request directly from the <a href='https://ms.portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade'>Reservation Blade</a>."
                }
            ]
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ]
}
---
