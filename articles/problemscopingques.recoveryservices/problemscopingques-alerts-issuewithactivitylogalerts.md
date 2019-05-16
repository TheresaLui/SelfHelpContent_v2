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
                        "visibility": "issue_type == Not getting Notification for alerts",
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
                      "visibility": "issue_type == Not getting Notification for alerts",
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
