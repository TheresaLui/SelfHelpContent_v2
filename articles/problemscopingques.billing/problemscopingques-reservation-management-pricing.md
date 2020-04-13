<properties
	articleId="Managed Reserved Instance-problemscopingquestion-pricing"
	pageTitle="Reservation Management- Pricing"
	description="Reservation Management- Pricing"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680684"
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
# Reservation Management- Pricing
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Reservation Management- Pricing",
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
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Select the Reservation Order ID",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/providers/Microsoft.Capacity/reservationOrders?api-version=2017-11-01",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,name",
                "textTemplate": "{properties.displayName} : {name}",
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
            "order": 7,
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
                    "value": "dont_know_answer",
                    "text": "Please enter the Reservation ID below"
                }
            ],
            "useAsAdditionalDetails": false,
            "required": true,
            "visibility": "reservationOrderId != null"
        },
        {
            "id": "reservationorderid_details",
            "order": 3,
            "visibility": "Reservationid == dont_know_answer",
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
                    "text": "Learn more on <a href='https://azure.microsoft.com/pricing/reserved-vm-instances/'>RI pricing</a>."
                },
		   {
                    "text": "Learn more on <a href='https://docs.microsoft.com/azure/billing/billing-understand-vm-reservation-charges'>RI discounts</a>."
                },
                {
                    "text": "Returns and exchanges can be done via self-service option directly from the <a href='https://ms.portal.azure.com/#blade/Microsoft_Azure_Reservations/ReservationsBrowseBlade'>Reservation Blade</a>."
                },
                {
                    "text": "Learn more - <a href='https://docs.microsoft.com/azure/billing/billing-azure-reservations-self-service-exchange-and-refund'>Self-service exchanges and refunds for azure reservations</a>."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
