<properties
         pageTitle="Scoping questions for Issue with Activity Log alerts"
         description="Scoping questions for Issue with Activity Log alerts"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632782"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
     	 articleId="3e888a24-bd39-4d22-9e30-82b4159728ad"
/>
# Questions for Issue with Activity Log alerts
---
{
         "resourceRequired": true,
	 "subscriptionRequired": true,
         "title": "Issue with Activity Log alerts",
         "fileAttachmentHint": "Please attach the screenshot of Activity Log alert screen filtered with timespan",
         "formElements": [{
                          "id": "issue_type",
                          "order": 1,
                          "visibility": "null",
                          "controlType": "dropdown",
                          "displayLabel": "Which type of issue your are facing?",
               		"dropdownOptions": [{
						"value": "Unable to see backup alerts in Azure portal",
						"text": "Unable to see backup alerts in Azure portal"
					},{
						"value": "Not receiving email notification for alerts",
						"text": "Not receiving email notification for alerts"
					},{
						"value": "dont_know_answer",
						"text": "Other, don't know or not applicable"
					}
					],
					"required": true
	},{
			"id": "email_address_confirmation",
			"order": 2,
			"visibility": "issue_type == Not receiving email notification for alerts",
			"controlType": "dropdown",
			"displayLabel": "Have you reverified the email address configured for alert?",
			"watermarkText": "Select",
			"dropdownOptions": [{
						"value": "Yes, it's correct",
						"text": "Yes, it's correct"
				},{
						"value": "No, i haven't reverified",
						"text": "No, i haven't reverified"
				},{
						"value": "dont_know_answer",
						"text": "Other, don't know or not applicable"
				}
			 ],
			 "required": true
	},{
			"id": "different_email_confirmation",
			"order": 3,
			"visibility": "issue_type == Not receiving email notification for alerts",
			"controlType": "dropdown",
			"displayLabel": "Have you tried getting notification on different email address?",
			"watermarkText": "Select",
			"dropdownOptions": [{
						"value": "Yes, it's working",
						"text": "Yes, it's working"
				},{
						"value": "Yes, it's not working",
						"text": "Yes, it's not working"
				},{
						"value": "No, i haven't tried",
						"text": "No, i haven't tried"
				},{
						"value": "dont_know_answer",
						"text": "Other, don't know or not applicable"
				}
			 ],
				"required": true
		},{
                      "id": "problem_start_time",
                      "order": 4,
                      "controlType": "datetimepicker",
                      "displayLabel": "When did the problem begin?",
                      "required": true
		},{
                      "id": "problem_description",
                      "order": 5,
                      "controlType": "multilinetextbox",
                      "useAsAdditionalDetails": true,
                      "displayLabel": "Additional details",
                      "watermarkText": "Provide additional information about your issue",
                      "required": true,
                      "hints": []
			      }
		  ]
}
---
