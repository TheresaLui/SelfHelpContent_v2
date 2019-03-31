<properties
	pageTitle="Reservation Management"
	description="Reservation Management"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32593231"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="reservationmanagement"
/>
# Reservation Management
---
{
    "resourceRequired": false,
    "title": "Reservation Management",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        },
        {
            "id": "reservation_instance_determination",
            "order": 2,
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "reservationorderid_details",
            "order": 3,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Reservation Order ID",
            "watermarkText": "Provide your Reservation Order id",
            "required": true
        },
        {
            "id": "reservationid_details",
            "order": 4,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Reservation ID",
            "watermarkText": "Provide your Reservation id",
            "required": true
        },
        {
            "id": "currentowner_details",
            "order": 5,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Current Owner",
            "watermarkText": "Provide the Current Owner details",
            "required": false
        },
        {
            "id": "newowner_details",
            "order": 6,
            "controlType": "textbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "New Owner",
            "watermarkText": "Provide the New Owner details",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "watermarkText": "Provide any additional information about your issue",
	    "displayLabel": "Additional details",
            "required": true
        }
    ]
}
---
