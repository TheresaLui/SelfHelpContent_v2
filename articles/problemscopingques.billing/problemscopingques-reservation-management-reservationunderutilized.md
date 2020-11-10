<properties
	articleId="Reservation Management-problemscopingques-reservation underutilized"
	pageTitle="Reservation Management-reservation underutilized"
	description="Reservation Management-reservation underutilized"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690275"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake, Fairfax, Blackforest, usnat, ussec"
	schemaVersion="1"
	ownershipId="ASMS_Billing"
/>
# Reservation Management-reservation underutilized
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Reservation Management-reservation underutilized",
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
            "order": 3,
            "visibility": "Reservationid == Other",
            "controlType": "textbox",
            "displayLabel": "Reservation ID",
            "watermarkText": "Provide your Reservation id",
            "required": false
        },
        {
            "id": "role_details",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "Your role on the subscription",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "error_details",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message/Screenshot of the error",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide any additional information about your issue",
            "required": true
	    }
    ],
    "$schema": "SelfHelpContent"
}
---
