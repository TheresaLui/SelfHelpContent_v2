<properties
         pageTitle="TSG Workflow Questions - Site-to-Site-VPN"
         description="Troubleshoot site-to-site VPN issues"
         authors="seanj-ms"
         ms.author="seanj"
         selfHelpType="TSG_Questions"
         productPesIds="15922"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="F2143039-B7F0-436B-B120-3C721FF0F4ED"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# TSG Workflow Questions
---
{
    "formElements": [
	{
            "id": "ae12a9a2-a04d-4dda-89e1-dad7914b4bf0",
            "order": 1,
            "controlType": "radioButtonGroup",
            "displayLabel": "What problem is the customer experiencing?",
            "radioButtonOptions": [
                {
                    "value": "VPN doesn't connect or never connected",
                    "text": "VPN doesn't connect or never connected"
                },
                {
                    "value": "VPN unstable - connects then disconnects",
                    "text": "VPN unstable - connects then disconnects"
                },
		{
                    "value": "VPN connects but resources unreachable",
                    "text": "VPN connects but resources unreachable"
                }
            ],
            "required": true
        },
        {
            "id": "2b27d3ad-6b77-4330-95d2-d68bfae16cec",
            "order": 2,
            "controlType": "radioButtonGroup",
            "displayLabel": "What type of VPN is the customer using?",
            "radioButtonOptions": [
                {
                    "value": "Route based - A supported route based device",
                    "text": "Route based - A supported route based device"
                },
                {
                    "value": "Policy based - A supported policy based device",
                    "text": "Policy based - A supported policy based device"
                }
            ],
            "required": true
        },
        {
            "id": "892ce993-13c4-4771-86d8-2f1868317a68",
            "order": 3,
            "controlType": "radioButtonGroup",
            "displayLabel": "Were you able to collect a log from diagnostics?",
            "radioButtonOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "There was no log to be found",
                    "text": "There was no log to be found"
                }
            ],
            "required": true
	},
        {
            "id": "1b6d04ad-2d19-4020-aa39-7d75ee39ac37",
            "order": 4,
            "controlType": "radioButtonGroup",
            "displayLabel": "Please select the error you found from running diagnostics",
            "radioButtonOptions": [
                {
                    "value": "13805 PeerReachability",
                    "text": "13805 PeerReachability"
                },
                {
                    "value": "13801 Authentication Pre-shared Key Mismatch",
                    "text": "13801 Authentication Pre-shared Key Mismatch"
                },
                {
                    "value": "13825/13868 IkePolicyMismatch",
                    "text": "13825/13868 IkePolicyMismatch"
                },
                {
                    "value": "13999 TSMismatch",
                    "text": "13999 TSMismatch"
                },
                {
                    "value": "13823/13824/13843 InvalidPayload",
                    "text": "13823/13824/13843 InvalidPayload"
                },
                {
                    "value": "13846 InvalidCookie",
                    "text": "13846 InvalidCookie"
                },
                {
                    "value": "13880 VersionMisMatch",
                    "text": "13880 VersionMisMatch"
                },
                {
                    "value": "1460 DpdTimeout",
                    "text": "1460 DpdTimeout"
                },
                {
                    "value": "13822 InvalidDHGroup",
                    "text": "13822 InvalidDHGroup"
                },
                {
                    "value": "Negotiation timed out",
                    "text": "Negotiation timed out"
                },
                {
                    "value": "I have an error but its not on this list",
                    "text": "I have an error but its not on this list"
                }
            ],
            "required": true
	},
        {
            "id": "d54dae25-4b82-4af3-b4f0-89e468e74bae",
            "order": 5,
            "controlType": "radioButtonGroup",
            "displayLabel": "Please select the root cause that's been diagnosed below",
            "radioButtonOptions": [
                {
                    "value": "On premise IP address was wrong",
                    "text": "On premise IP address was wrong"
                },
                {
                    "value": "Customer device isn't responding",
                    "text": "Customer device isn't responding"
                },
                {
                    "value": "Asymmetric routing",
                    "text": "Asymmetric routing"
                },
                {
                    "value": "Logs show packets from both sides of the connection",
                    "text": "Logs show packets from both sides of the connection"
                }
            ],
            "required": true
	},
        {
            "id": "8340b03f-634d-4fb4-b5a0-1412b68fb87d",
            "order": 6,
            "controlType": "radioButtonGroup",
            "displayLabel": "Please select the root cause that's been diagnosed below",
            "radioButtonOptions": [
                {
                    "value": "On premise IP address was wrong",
                    "text": "On premise IP address was wrong"
                },
                {
                    "value": "Customer device isn't responding",
                    "text": "Customer device isn't responding"
                },
                {
                    "value": "Asymmetric routing",
                    "text": "Asymmetric routing"
                },
                {
                    "value": "Logs show packets from both sides of the connection",
                    "text": "Logs show packets from both sides of the connection"
                }
            ],
            "required": true
	},
        {
            "id": "81d8eae1-c6c7-4cf6-a00d-85b601fb2c86",
            "order": 7,
            "controlType": "radioButtonGroup",
            "displayLabel": "Please select the root cause that's been diagnosed below",
            "radioButtonOptions": [
                {
                    "value": "On premise IP address was wrong",
                    "text": "On premise IP address was wrong"
                },
                {
                    "value": "Customer device isn't responding",
                    "text": "Customer device isn't responding"
                },
                {
                    "value": "Asymmetric routing",
                    "text": "Asymmetric routing"
                },
                {
                    "value": "Logs show packets from both sides of the connection",
                    "text": "Logs show packets from both sides of the connection"
                }
            ],
            "required": true
	},
        {
            "id": "09904fdf-533d-44aa-bf4d-03d7174915a1",
            "order": 8,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the VPN Gateway healthy?",
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
            "id": "852971af-9817-44e8-8583-3d26063a1a9f",
            "order": 9,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the VPN VIP and DIP healthy?",
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
            "id": "9a9e3877-d322-4a82-aa5c-56bf158e5efc",
            "order": 10,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the issue a known issues with 3rd party devices?",
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
            "id": "d65de7e6-69c6-4401-9b60-0b3c3f5dd930",
            "order": 11,
            "controlType": "radioButtonGroup",
            "displayLabel": "Were you able to collect a log from diagnostics?",
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
            "id": "0eef6f5a-a79a-4e7e-b7bb-ce543d98ea73",
            "order": 12,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is there an NSG on the gateway subnet?",
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
            "id": "dfaba41a-8b0c-47f0-ba53-99418e970258",
            "order": 13,
            "controlType": "radioButtonGroup",
            "displayLabel": "Did the steps above resolve the issue?",
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
            "id": "0f11055e-4407-47a5-9423-963233611b7d",
            "order": 14,
            "controlType": "radioButtonGroup",
            "displayLabel": "What type of VPN is the customer using?",
            "radioButtonOptions": [
                {
                    "value": "Route based",
                    "text": "Route based"
                },
                {
                    "value": "Policy based",
                    "text": "Policy based"
                }
            ],
            "required": true
	},
	{
            "id": "7519526a-a0e5-44f9-a06c-e6b3dccc722f",
            "order": 15,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the customer exceeding the maximum number of SAs?",
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
            "id": "f1f18cfd-1a58-4f22-a39a-9710721261b3",
            "order": 16,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the customer using narrow traffic selectors on the Azure side?",
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
            "id": "523e30c4-04e1-41b6-987a-3714785de772",
            "order": 17,
            "controlType": "radioButtonGroup",
            "displayLabel": "Are Traffic Selectors incorrectly configured on customer device?",
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
            "id": "9155c5c4-88e3-4a1b-ac19-ee7c27bc661d",
            "order": 18,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the on-prem device incorrectly configuring the traffic selectors?",
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
            "id": "9ecb6aa8-b9df-485a-81e7-d5b77f8c147d",
            "order": 19,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the Azure VPN gateway incorrectly configuring the traffic selectors?",
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
            "id": "188ce3eb-0a2a-49b1-aaf6-d8e522b58adc",
            "order": 20,
            "controlType": "radioButtonGroup",
            "displayLabel": "Were you able to identify an error?",
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
            "id": "4d3ee1ab-0171-456f-81a9-ee7a7d06e678",
            "order": 21,
            "controlType": "radioButtonGroup",
            "displayLabel": "Please select the root cause that's been diagnosed below",
            "radioButtonOptions": [
                {
                    "value": "The IP Address of the on-prem device was incorrect",
                    "text": "The IP Address of the on-prem device was incorrect"
                },
                {
                    "value": "The customer did not create a connection object",
                    "text": "The customer did not create a connection object"
                },
		{
                    "value": "The SiteConnectivityAction flag was set to Disconnect",
                    "text": "The SiteConnectivityAction flag was set to Disconnect"
                },
		{
                    "value": "Everything is correct - none of these options apply",
                    "text": "Everything is correct - none of these options apply"
                }
            ],
            "required": true
	},
	{
            "id": "e9c6722a-1e01-4dd8-bd71-b1da132a2eda",
            "order": 22,
            "controlType": "radioButtonGroup",
            "displayLabel": "Was the failover a planned maintenance?",
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
            "id": "07f4027a-b0e8-4009-b984-330e0f5d48ae",
            "order": 23,
            "controlType": "radioButtonGroup",
            "displayLabel": "Was it maintenance or customer reset that caused the tunnel state change reason?",
            "radioButtonOptions": [
                {
                    "value": "Customer",
                    "text": "Customer"
                },
                {
                    "value": "Maintenance",
                    "text": "Maintenance"
                }
            ],
            "required": true
	},
	{
            "id": "395ec88d-e3ad-4303-bc9d-137fb9cf9627",
            "order": 24,
            "controlType": "radioButtonGroup",
            "displayLabel": "What is the tunnel state change reason (TunnelStateChangeReason)?",
            "radioButtonOptions": [
                {
                    "value": "RemotelyTriggered / RemoteCrashTriggered",
                    "text": "RemotelyTriggered / RemoteCrashTriggered"
                },
                {
                    "value": "DPD timed out / Main mode SA assumed to be invalid because peer stopped responding",
                    "text": "DPD timed out / Main mode SA assumed to be invalid because peer stopped responding"
                },
		{
                    "value": "IKE authentication credentials are unacceptable / Pre-shared Key Changed",
                    "text": "IKE authentication credentials are unacceptable / Pre-shared Key Changed"
                },
		{
                    "value": "DhGroup changed / EncryptionType changed / IkeIntegrity changed / PfsGroup changed / SALifetimeSeconds changed / SALifeKilloBytes changed / UseNarrowTrafficSelectors changed / NarrowTSEnabled changed",
                    "text": "DhGroup changed / EncryptionType changed / IkeIntegrity changed / PfsGroup changed / SALifetimeSeconds changed / SALifeKilloBytes changed / UseNarrowTrafficSelectors changed / NarrowTSEnabled changed"
                },
		{
                    "value": "Invalid payload received / Error processing Notify payload / Error processing KE payload / Require configuration payload missing",
                    "text": "Invalid payload received / Error processing Notify payload / Error processing KE payload / Require configuration payload missing"
                },
		{
                    "value": "IKE SA deleted before establishment completed",
                    "text": "IKE SA deleted before establishment completed"
                },
		{
                    "value": "TunnelRemoved",
                    "text": "TunnelRemoved"
                },
		{
                    "value": "Unknown / other error",
                    "text": "Unknown / other error"
                }
            ],
            "required": true
	},
	{
            "id": "e749500d-6a81-4160-91f3-bfa668bb800d",
            "order": 25,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the customer's device in the supported device list?",
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
            "id": "9c56aba3-0f21-4014-b4c0-fcdb11e5bbf1",
            "order": 26,
            "controlType": "radioButtonGroup",
            "displayLabel": "Does the customer's config match the VPN device script?",
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
            "id": "af0b2508-eee1-417e-bf8a-4a992ae3d558",
            "order": 27,
            "controlType": "radioButtonGroup",
            "displayLabel": "Please select the error you found from diagnostics",
            "radioButtonOptions": [
                {
                    "value": "ERROR_IPSEC_IKE_TIMED_OUT / 0x000035ed  / Negotiation Timed out /Main mode SA assumed to be invalid because peer stopped responding / ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID / 0x0000363e",
                    "text": "ERROR_IPSEC_IKE_TIMED_OUT / 0x000035ed  / Negotiation Timed out /Main mode SA assumed to be invalid because peer stopped responding / ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID / 0x0000363e"
                },
                {
                    "value": "IKE authentication credentials are unacceptable / PSK auth verification failed / ERROR_IPSEC_IKE_INVALID_SIGNATURE / 0x00003602 / Failed to verify signature / ERROR_IPSEC_IKE_AUTH_FAIL / 0x000035e9",
                    "text": "IKE authentication credentials are unacceptable / PSK auth verification failed / ERROR_IPSEC_IKE_INVALID_SIGNATURE / 0x00003602 / Failed to verify signature / ERROR_IPSEC_IKE_AUTH_FAIL / 0x000035e9"
                },
                {
                    "value": "Processing LIFETIME change QM Notify / 0x80073610 / ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY",
                    "text": "Processing LIFETIME change QM Notify / 0x80073610 / ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"
                },
                {
                    "value": "Policy Match Error / ERROR_IPSEC_IKE_POLICY_MATCH / 0x0000362c / Remote Auth method 0 not supported by policy / Peer sent NO_PROPOSAL_CHOSEN notify",
                    "text": "Policy Match Error / ERROR_IPSEC_IKE_POLICY_MATCH / 0x0000362c / Remote Auth method 0 not supported by policy / Peer sent NO_PROPOSAL_CHOSEN notify"
                },
		{
                    "value": "Received MM delete / peer sent a main mode delete / 0x0000363d",
                    "text": "Received MM delete / peer sent a main mode delete / 0x0000363d"
                },
                {
                    "value": "ERROR_IPSEC_IKE_INVALID_PAYLOAD / 0x80073613",
                    "text": "ERROR_IPSEC_IKE_INVALID_PAYLOAD / 0x80073613"
                },
                {
                    "value": "ERROR_IPSEC_IKE_INVALID_COOKIE / 0x00003616 / 0x80073616",
                    "text": "ERROR_IPSEC_IKE_INVALID_COOKIE / 0x00003616 / 0x80073616"
                },
                {
                    "value": "IKE Version Mismatch",
                    "text": "IKE Version Mismatch"
                },
                {
                    "value": "Gateway not sending IPsec traffic / No policy configured / ERROR_IPSEC_IKE_NO_POLICY / 0x00003601 / Construct CERT REQUEST / Process Payload CERTREQ",
                    "text": "Gateway not sending IPsec traffic / No policy configured / ERROR_IPSEC_IKE_NO_POLICY / 0x00003601 / Construct CERT REQUEST / Process Payload CERTREQ"
                },
		{
                    "value": "Idle Timeout",
                    "text": "Idle Timeout"
                },
                {
                    "value": "DoS mode on / Sending DoS Cookie Notify",
                    "text": "DoS mode on / Sending DoS Cookie Notify"
                }
            ],
            "required": true
	},
        {
            "id": "c524b80a-98cb-4b73-a2c9-cfaf2a125b40",
            "order": 28,
            "controlType": "radioButtonGroup",
            "displayLabel": "Please select the error you found from running diagnostics",
            "radioButtonOptions": [
                {
                    "value": "ERROR_IPSEC_IKE_TIMED_OUT / 0x000035ed  / Negotiation Timed out /Main mode SA assumed to be invalid because peer stopped responding / ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID / 0x0000363e",
                    "text": "ERROR_IPSEC_IKE_TIMED_OUT / 0x000035ed  / Negotiation Timed out /Main mode SA assumed to be invalid because peer stopped responding / ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID / 0x0000363e"
                },
                {
                    "value": "IKE authentication credentials are unacceptable / PSK auth verification failed / ERROR_IPSEC_IKE_INVALID_SIGNATURE / 0x00003602 / Failed to verify signature / ERROR_IPSEC_IKE_AUTH_FAIL / 0x000035e9",
                    "text": "IKE authentication credentials are unacceptable / PSK auth verification failed / ERROR_IPSEC_IKE_INVALID_SIGNATURE / 0x00003602 / Failed to verify signature / ERROR_IPSEC_IKE_AUTH_FAIL / 0x000035e9"
                },
                {
                    "value": "Processing LIFETIME change QM Notify / 0x80073610 / ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY",
                    "text": "Processing LIFETIME change QM Notify / 0x80073610 / ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"
                },
                {
                    "value": "Policy Match Error / ERROR_IPSEC_IKE_POLICY_MATCH / 0x0000362c / Remote Auth method 0 not supported by policy",
                    "text": "Policy Match Error / ERROR_IPSEC_IKE_POLICY_MATCH / 0x0000362c / Remote Auth method 0 not supported by policy"
                },
                {
                    "value": "ERROR_IPSEC_IKE_INVALID_PAYLOAD / 0x80073613",
                    "text": "ERROR_IPSEC_IKE_INVALID_PAYLOAD / 0x80073613"
                },
                {
                    "value": "ERROR_IPSEC_IKE_INVALID_COOKIE / 0x00003616 / 0x80073616",
                    "text": "ERROR_IPSEC_IKE_INVALID_COOKIE / 0x00003616 / 0x80073616"
                },
                {
                    "value": "IKE Version Mismatch",
                    "text": "IKE Version Mismatch"
                },
                {
                    "value": "Gateway not sending IPsec traffic / No policy configured / ERROR_IPSEC_IKE_NO_POLICY / 0x00003601 / Construct CERT REQUEST / Process Payload CERTREQ",
                    "text": "Gateway not sending IPsec traffic / No policy configured / ERROR_IPSEC_IKE_NO_POLICY / 0x00003601 / Construct CERT REQUEST / Process Payload CERTREQ"
                },
                {
                    "value": "No errors - No IKE negotiation packets observed on the logs",
                    "text": "No errors - No IKE negotiation packets observed on the logs"
                }
            ],
            "required": true
	},
    ],
    "$schema": "SelfHelpContent"
}
---