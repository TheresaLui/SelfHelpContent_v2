<properties
	pageTitle="Cluster Certificates"
	description="Cluster Certificates"
	authors="peterpogorski"
	ms.author="pepogors"
	selfHelpType="ProblemScopingQuestions"
	supportTopicIds="32608942, 32608944, 32608943, 32608957"
	productPesIds="15842"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-cluster-certificate-sf"
	ownershipId="Compute_ServiceFabric"
/>
# Cluster Certificate
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Cluster Certificates",
    "formElements": [{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "Incident time",
			"required": true
		},
		{
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
			"required": true,
			"useAsAdditionalDetails": true
		},
        {
            "id": "certificate_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel":  "Is the certificate that is used to secure your cluster CA signed or self-signed?",
            "watermarkText":  "Choose an option",
            "dropdownOptions": [{
                "value": "The certificate is signed by a Certificate Authority",
                "text": "The certificate is signed by a Certificate Authority"
            },{
                "value": "The certificate is self-signed",
                "text": "The certificate is self-signed"
            }],
            "required": false
        },
        {
            "id": "certificate_management",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is your cluster secured using certificate thumbprint or using certificate common name?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                "value": "Certificate common name and issuer thumbprint",
                "text": "Certificate common name and issuer thumbprint"
            },
            {
                "value": "Certificate thumbprint",
                "text": "Certificate thumbprint"
            }],
            "required": false
        },
        {
            "id": "get_certificate_thumbprint",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the thumbprints of the subjective certificate(s)",
            "watermarkText": "If you are replacing an old certificate with a new one, please specify the thumbprint of both certificates.",
            "required": false
        }
	],
    "$schema": "SelfHelpContent"
}
---