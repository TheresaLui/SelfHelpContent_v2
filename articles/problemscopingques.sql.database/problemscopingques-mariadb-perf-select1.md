<properties
	pageTitle="Database Performance"
	description="Database Performance"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628372"
	productPesIds="16617"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-mariadb-perf-select1"
/>
# Database Performance - SELECT 1
---

{
	"resourceRequired": false,
	"subscriptionRequired": false,
	"title": "Database SELECT 1 Performance",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "repro_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When was the most recent repro?",
			"required": true
		}, {
			"id": "persistent",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Are you having a consistent repro?",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
		}, {
            "id": "select_1",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your select 1 performance latency?",
            "required": false
        }, {
            "id": "client_location",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "Is your client located in the same region as your database server?",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
        }, {
            "id": "pooling",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Do you have connection pooling enabled?",
            "infoBalloonText": "It is highly recommended to enable connection pooling tools while testing the server performance with multiple connections.",
            "dropdownOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        }, {
            "id": "accelerated_networking",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Is accelerated networking enabled on the client?",
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}
			],
			"required": false
        }, {
			"id": "point_of_comparison",
			"order": 8,
			"controlType": "dropdown",
			"displayLabel": "What is your point of comparison?",
			"dropdownOptions": [{
                    "value": "It is slower than it typically is",
                    "text": "It is slower than it typically is"
                }, {
                    "value": "It is slower than another database server on Azure",
                    "text": "It is slower than another database server on Azure"
                }, {
                    "value": "It is slower when connection is from VNET",
                    "text": "It is slower when connection is from VNET"
                }, {
                    "value": "It is slower than server on Non Azure Environment",
                    "text": "It is slower than server on Non Azure Environment"
                }, {
                    "value": "It is slower than database server running on VM/Locally",
                    "text": "It is slower than database server running on VM/Locally"
                }, {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
			"required": true
		}, {
            "id": "other_point_of_comparison",
            "order": 9,
            "visibility": "point_of_comparison == Other",
            "controlType": "textbox",
            "displayLabel": "Please specify your point of comparison:",
            "required": false
        }, {
            "id": "measurement_tool",
            "order": 10,
            "controlType": "textbox",
            "displayLabel": "What tool are you using to measure your performance??",
            "watermarkText": "e.g. SysBench",
            "required": false
        }, {
			"id": "problem_description",
			"order": 11,
			"controlType": "multilinetextbox",
			"displayLabel": "Problem description",
			"watermarkText": "Provide your repro steps and other information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}

---
