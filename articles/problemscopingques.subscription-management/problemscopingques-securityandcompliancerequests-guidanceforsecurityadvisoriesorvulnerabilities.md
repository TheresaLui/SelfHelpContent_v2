<properties
	pageTitle="Security and Compliance Requests"
	description="Security and Compliance Requests"
	authors="prdasneo"
	authorAlias="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32611254"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="guidanceforsecurityadvisoriesorvulnerabilities"
/>


# GUIDANCE FOR SECURITY ADVISORIES OR VULNERABILITIES
---
{
    "resourceRequired": false,
    "title": "Guidance for security advisories or vulnerabilities",
    "fileAttachmentHint": "",
    "formElements": [
					  {
						  "id": "problem_start_time",
						  "visibility": null,
						  "order": 1,
						  "controlType": "datetimepicker",
						  "displayLabel": "When did the problem start?",
						  "content": null,
						  "watermarkText": null,
						  "infoBalloonText": null,
						  "dropdownOptions": null,
						  "dynamicDropdownOptions": null,
						  "hints": [],
						  "required": true,
						  "maxLength": 0,
						  "useAsAdditionalDetails": false,
						  "numberOfLines": 0
					  },
				      {
							"id": "problem_description",
							"order": 3,
							"controlType": "multilinetextbox",
							"displayLabel": "Please provide these details",
							"required": true,
							"useAsAdditionalDetails": true,
								"hints": [{
										"text": "Azure Service impacted"
									}
								]
					  },
					  {
							"id": "subscription_id_determination",
							"order": 2,
							"controlType": "dropdown",
							"displayLabel": "Please select the subscription id",
							"watermarkText": "Choose an option",
							"dynamicDropdownOptions": 
								{
									"uri": "/subscriptions?api-version=2014-04-01?",
									"jTokenPath": "value",
									"textProperty": "name",
									"valueProperty": "id",
									"textPropertyRegex": "[^/]+$"
								}
						}	
					]
					
}
					
---
