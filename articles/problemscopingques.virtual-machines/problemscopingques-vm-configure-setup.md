<properties
	pageTitle="Virtual Machine Configure"
	description="Virtual Machine Configure"
	authors="phgantik"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32411855,32411856,32411853,32411844,32411835,32549256,32411817,32411820,32573480,32411816,32588972,32588969,32588977,32588975,32567269,32567274,32584248,32547225"
	productPesIds="15571,15797,14749,16098,16215,15526"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Availability Zones for VMs
---
{
	"resourceRequired": true,
	"title": "Availability Zones",
	"fileAttachmentHint": "",
	"formElements": 
	[{
			"id": "Availability_Zones",
			"order": 1,
			"controlType": "dropdown",
			"displayLabel": "Is the Service in an Availability Zones",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				} 
			"required": true
		}, 
		{
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}
	]
}
---
