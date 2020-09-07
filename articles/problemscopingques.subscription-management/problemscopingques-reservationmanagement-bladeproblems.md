<properties
	pageTitle="ReservationManagement-Blade Issues"
	description="ReservationManagement-Blade Issues"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680693"
	productPesIds="15660"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="reservationmanagmentbladeissues-problemscopingquestions"
	ownershipId="ASMS_SubscriptionManagement"
/>

# ReservationManagement-Blade Issues
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
            "visibility": "Reservationid == Other",
            "controlType": "textbox",
            "displayLabel": "Reservation ID",
            "watermarkText": "Provide your Reservation id",
            "required": false
        },
        {
            "id": "role_details",
            "order":6,
            "controlType": "textbox",
            "displayLabel": "Your role on the reservation",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "browser_details1",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Browser Information",
            "watermarkText": "Choose the browser",
            "dropdownOptions": [
                {
                    "value": "Apple Safari",
                    "text": "Apple Safari"
                },
                {
                    "value": "Google Chrome",
                    "text": "Google Chrome"
                },
                {
                    "value": "Internet Explorer",
                    "text": "Internet Explorer"
                },
                {
                    "value": "Microsoft Edge",
                    "text": "Microsoft Edge"
                },
                {
                    "value": "Mozilla Firefox",
                    "text": "Mozilla Firefox"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "browser_details2",
            "order": 8,
            "visibility": "browser_details1 == dont_know_answer",
            "controlType": "textbox",
            "displayLabel": "Please provide the Browser Information",
            "required": false
        },
        {
            "id": "error_details",
            "order":9,
            "controlType": "multilinetextbox",
            "displayLabel": "Error Message/Screenshot of the issue",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 10,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Browser network trace or any other details (if applicable)",
            "watermarkText": "Provide the browser network trace or any additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Learn more - <a href='https://blogs.msdn.microsoft.com/benjaminperkins/2016/10/18/capture-a-trace-for-troubleshooting-azure-portal-issues/'>how to capture a browser network trace</a>"
                }
                ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
