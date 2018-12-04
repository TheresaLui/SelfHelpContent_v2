<properties
	pageTitle="Reservation Management"
	description="Reservation Management"
	authors="prdasneo"
	authorAlias="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32593233"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="otherissuesorrequests"
/>


# OTHER ISSUES OR REQUESTS
---
{
    "resourceRequired": false,
    "title": "Other issues or requests",
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
            "hints": [{
					"text": "Reservation Order ID"
				},
				{
					"text": "Reservation ID"
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
