<properties
         pageTitle="TSG Workflow Questions - 502 Gateway Error"
         description="Troubleshoot 502 Gateway Error issues"
         authors="seanj-ms"
         ms.author="seanj"
         selfHelpType="TSG_Questions"
         productPesIds="15922"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="D88F3F43-0CC3-4143-ACED-C4820B56E8EC"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# TSG V2 Workflow Questions Test
---
{
    "formElements": [
        {
            "id": "cc74431c-174a-45c6-93f8-7985291eb567",
            "order": 1,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the backend pool empty?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "e0587a42-0e33-4d3b-ba91-66600bb3c90c",
            "order": 2,
            "controlType": "radioButtonGroup",
            "displayLabel": "Are all the backend servers unhealthy?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
        {
            "id": "20e27905-6a8c-4003-9ff7-bc8bfd9957e9",
            "order": 3,
            "controlType": "radioButtonGroup",
            "displayLabel": "What is the SSL related error?",
            "radioButtonOptions": [
                {
                    "value": "V1 SKU: Backend Server Certificate needs to be whitelisted in Application Gateway",
                    "text": "V1 SKU: Backend Server Certificate needs to be whitelisted in Application Gateway"
                },
                {
                    "value": "V1 SKU: Https probe connection error",
                    "text": "V1 SKU: Https probe connection error"
                },
                {
                    "value": "V2 SKU: The common name (CN) of the backend certificate does not match the host header",
                    "text": "V2 SKU: The common name (CN) of the backend certificate does not match the host header"
                },
                {
                    "value": "V2 SKU: The server certificate used by the backend is not signed by a well-known Certificate Authority (CA)",
                    "text": "V2 SKU: The server certificate used by the backend is not signed by a well-known Certificate Authority (CA)"
                },
                {
                    "value": "V2 SKU: The root certificate of the server certificate used by the backend does not match the trusted root certificate added to the application gateway",
                    "text": "V2 SKU: The root certificate of the server certificate used by the backend does not match the trusted root certificate added to the application gateway"
                },
                {
                    "value": "V2 SKU: The validity of the backend certificate could not be verified",
                    "text": "V2 SKU: The validity of the backend certificate could not be verified"
                },
                {
                    "value": "V2 SKU: Backend certificate is invalid. Current date is not within the \"Valid from\" and \"Valid to\" date range on the certificate",
                    "text": "V2 SKU: Backend certificate is invalid. Current date is not within the \"Valid from\" and \"Valid to\" date range on the certificate"
                },
                {
                    "value": "Not an SSL related error",
                    "text": "Not an SSL related error"
                }
            ],
            "required": true
		},
        {
            "id": "6eceee09-c605-4bda-8334-37f08840bcaa",
            "order": 4,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is there a custom probe configured for the HTTP Setting?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
		},
    ],
    "$schema": "SelfHelpContent"
}
---