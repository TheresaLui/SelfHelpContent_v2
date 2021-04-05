<properties
	pageTitle="Azure Defender - Regulatory Compliance Management"
	description="Azure Defenderr - Regulatory Compliance Management"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32693246"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_regulatorycompliancemanagement"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Configuring Features and Resources - Just-in-time access (JIT)
---
{
				"$schema": "SelfHelpContent",
                "resourceRequired": false,
                "title": "Regulatory Compliance Management",
				"subscriptionRequired": false,
                "formElements": [
                {
                "id": "init_name",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "What is the name of the regulatory compliance assigned to your subscription?",
                "required": true
                },{
                    "id": "problem_description",
                    "order": 1,
                    "controlType": "multilinetextbox",
                    "displayLabel": "Description",
                    "useAsAdditionalDetails": true,
                    "required": true
                    },{
                    "id": "problem_start_time",
                    "order": 8,
                    "controlType": "datetimepicker",
                    "displayLabel": "When did the problem start?",
                    "required": true
                  }
                  ]
}
---
