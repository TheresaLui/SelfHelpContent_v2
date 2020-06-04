<properties
	articleId="5c780e90-4ac8-443a-8aef-96e473e93424"
	pageTitle="Scoping Questions for HDInsight Authentication with Ambari in ESP Issue"
	description="Scoping Questions for HDInsight Authentication with Ambari in ESP Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636436"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HDInsight Authentication with Ambari in ESP Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight HDFS Authentication with Ambari in ESP Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "bypass_conditional_access",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "Have you configured conditional access policy to be bypassed for the cluster login? Have you disabled Multi-Factor Authentication?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "aad_endpoint",
            "visibility": "bypass_conditional_access == No",
            "order": 100,
            "controlType": "dropdown",
            "displayLabel": "Has the AAD service endpoint been enabled to allow traffic from HDInsight VNet?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "account_federation",
            "order": 150,
            "controlType": "dropdown",
            "displayLabel": "Are the accounts federated?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "ADFS",
                    "text": "ADFS"
                },
                {
                    "value": "Third_Party",
                    "text": "Third Party"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "user_scope",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "Does the issue affect all users or a few users?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "All_users",
                    "text": "All users"
                },
                {
                    "value": "Few_users",
                    "text": "A few users"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "service_scope",
            "order": 250,
            "controlType": "dropdown",
            "displayLabel": "Does the user account work with other Azure services?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "kinit",
            "order": 300,
            "controlType": "dropdown",
            "displayLabel": "Does kinit for some or all users work from the Head node?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "clusteradmin",
            "order": 310,
            "controlType": "dropdown",
            "displayLabel": "Does authentication fail even for the cluster admin account?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "usersync",
            "order": 350,
            "controlType": "dropdown",
            "displayLabel": "Have you logged in to Ambari as local admin and verified the users have been synced?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text, exception callstack if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
