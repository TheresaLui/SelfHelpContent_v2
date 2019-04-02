<properties
	articleId="b4b6273d-558e-4f2d-ab00-36a830ea4353"
	pageTitle="Reservation Management"
	description="Reservation Management"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32593227,32593228,32593229"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake"
	schemaVersion="1"
/>
# Reservation Management
---
{
   "resourceRequired": false,
    "subscriptionRequired": true,
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
            "id": "Reservationid",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Select the Reservation ID",
            "dynamicDropdownOptions": {
             "uri": "/subscriptions/{subscriptionid}/Microsoft.Capacity/appliedReservations?api-version=2014-04-01",
             "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": null,
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of reservations.",
                    "text": "Unable to retrieve list of reservations"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "reservationorderid_details",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Reservation Order ID",
            "watermarkText": "Provide your Reservation Order id",
            "required": false
        },
        {
            "id": "reservationid_details",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Reservation ID",
            "watermarkText": "Provide your Reservation id",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
	    "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide any additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Note: To ensure we capture all of your reservation details accurately, please raise a service request directly from the <a href='https://ms.portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade'>Reservation Blade</a>."
                }
            ]
        }
    ]
}
---
