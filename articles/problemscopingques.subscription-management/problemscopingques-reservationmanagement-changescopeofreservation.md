<properties
	pageTitle="Reservation Management"
	description="Reservation Management"
	authors="prdasneo"
	authorAlias="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32593232"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="changescopeofreservation"
/>


# CHANGE SCOPE OF RESERVATION
---
{
    "resourceRequired": false,
    "title": "Change scope of reservation",
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
					"text": "This can be Self served .For any other concern, please provide a brief description in the details section."
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
