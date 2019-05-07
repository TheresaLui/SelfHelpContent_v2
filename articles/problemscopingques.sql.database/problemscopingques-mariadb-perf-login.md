<properties
	pageTitle="Database Performance"
	description="Database Performance"
	authors="Xin-Cheng"
	ms.author="chengxin"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640126"
	productPesIds="16617"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-mariadb-perf-login"
/>
# Database Performance - login
---
{
	"resourceRequired": false,
	"subscriptionRequired": false,
	"title": "Database login is slow",
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
            "id": "client_location",
			"order": 3,
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
            "id": "accelerated_networking",
			"order": 4,
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
            "id": "pooling",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Do you have connection pooling enabled?",
            "infoBalloonText": "It is highly recommended to enable connection pooling while testing the server performance with multiple connections.",
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
			"order": 6,
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
            "order": 7,
            "visibility": "point_of_comparison == Other",
            "controlType": "textbox",
            "displayLabel": "Please specify your point of comparison:",
            "required": false
        }, {
            "id": "workload",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Is the workload the same as your point of comparison?",
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
            "id": "measurement_method",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "What tools are you using to measure your performance?",
            "required": false
        }, {
            "id": "measurement",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide your performance/latency numbers:",
            "required": false
        }, {
            "id": "login_happens_at",
            "order": 11,
            "controlType": "dropdown",
            "displayLabel": "Login latency happens at:",
            "dropdownOptions": [{
                    "value": "First Login",
                    "text": "First Login"
                }, {
                    "value": "Every Login",
                    "text": "Every Login"
                }, {
					"value": "dont_know_answer",
					"text": "I don't know"
				}
            ],
            "required": true
        }, {
			"id": "problem_description",
			"order": 12,
			"controlType": "multilinetextbox",
			"displayLabel": "Problem description",
			"watermarkText": "Provide your repro steps and other information about your issue",
			"required": true,
			"useAsAdditionalDetails": true
		}
	]
}

---
