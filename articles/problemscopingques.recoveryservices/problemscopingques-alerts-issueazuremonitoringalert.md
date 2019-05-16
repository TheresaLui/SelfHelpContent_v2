<properties
         pageTitle="Scoping questions for Issue with Azure Monitoring alerts (rule based)"
         description="Scoping questions for Issue with Azure Monitoring alerts (rule based)"
         authors="srinathvasireddy"
		     ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632783"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
		     articleId="581fcaaa-2d8f-4897-8dba-20e19a78926e"
/>
# Questions for Issue with Azure Monitoring alerts (rule based)
---
{
         "resourceRequired": true,
		     "subscriptionRequired": true,
         "title": "Issue with Azure Monitoring alerts (rule based)",
         "fileAttachmentHint": "Please attach the screenshot of Alert screen filtered with timespan",
		      "formElements": [{
							"id": "issue_type",
							"order": 1,
							"visibility": "null",
							"controlType": "multiselectdropdown",
							"displayLabel": "Which type of issue your are facing?",
							"dropdownOptions": [{
												"value": "Not getting backup alerts in Azure portal",
												"text": "Not getting backup alerts in Azure portal"
											},{
												"value": "Not getting Notification for alerts",
												"text": "Not getting Notification for alerts"
											},{
												"value": "dont_know_answer",
												"text": "Other, don't know or not applicable"
											}
											],
											"required": true
						},{
						 	"id": "email_address_confirmation",
							"order": 2,
							"visibility": "issue_Type == Not getting Notification for alerts",
							"controlType": "dropdown",
							"displayLabel": "Have you reverified the Email address configured for alert?",
							"watermarkText": "Select",
							"dropdownOptions": [{
												"value": "Yes",
												"text": "Yes"
										},{
												"value": "No",
												"text": "No"
										},{
												"value": "dont_know_answer",
												"text": "Other, don't know or not applicable"
										}
									 ],
									 "required": true
					},{
							"id": "different_email_confirmation",
							"order": 3,
							"visibility": "issue_Type == Not getting Notification for alerts",
							"controlType": "dropdown",
							"displayLabel": "Have you tried to get notification on different Email address?",
							"watermarkText": "Select",
							"dropdownOptions": [{
												"value": "Yes",
												"text": "Yes"
										},{
												"value": "No",
												"text": "No"
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
