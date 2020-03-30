<properties
	pageTitle="Reservation Management"
	description="Reservation Management"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690276"
	productPesIds="15660"
	cloudEnvironments="public, Mooncake, Blackforest, Fairfax"
	schemaVersion="1"
	articleId="b4b6273d-558e-4f2d-ab00-36a830ea4369"
	ownershipId="ASMS_SubscriptionManagement"
/>

# Other Issues or Requests
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
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
                    "value": "Cosmos DB",
                    "text": "Cosmos DB"
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
            "id": "reservationOrderId",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the Reservation Order ID",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/providers/Microsoft.Capacity/reservationOrders?api-version=2017-11-01",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,name",
                "textTemplate": "{properties.displayName} ({name})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Unable to retrieve list of reservations",
                    "text": "Unable to retrieve list of reservations"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true
        },
        {
            "id": "Reservationid",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Select the Reservation ID",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/providers/Microsoft.Capacity/reservationOrders/{replaceWithParentValue}/reservations?api-version=2017-11-01",
                "jTokenPath": "value",
                "dependsOn": "reservationOrderId",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
		"valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "dropdownOptions": [
                {
                    "value": "Other",
                    "text": "Please enter the Reservation ID below"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true,
            "visibility": "reservationOrderId != null"
        },
        {
            "id": "reservationorderid_details",
            "order": 5,
            "visibility": "Reservationid == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Reservation ID",
            "watermarkText": "Provide your Reservation id",
            "required": false
        },
	{
            "id": "currentowner_details",
            "order":6,
            "controlType": "textbox",
            "displayLabel": "Current Owner",
            "watermarkText": "",
            "required": false
        },
	{
            "id": "newowner_details",
            "order":7,
            "controlType": "textbox",
            "displayLabel": "New Owner",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide any additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Returns and exchanges can be done via **self-service option** directly from the <a href='https://ms.portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade'>Reservation Blade</a>. Learn more - <a href='https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund'>here</a>"
                },
                {
                    "text": "To request a billing related request, please select the Issue type as **Billing** and Problem type as **Reservation management** to ensure faster resolution"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
