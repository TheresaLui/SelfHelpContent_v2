<properties
	pageTitle="EmbeddedCSDKIssues"
	description="Embedded-C-SDK-Issues"
	service="microsoft.devices"
	resource="IoTSDKs"
	authors="wduraes"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596697"
	resourceTags=""
	productPesIds="16122"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	articleId="61c54bbd-c2c6-5271-96e7-009a87ff44bf"
	ownershipId="AzureIot_IotHub"
/>

# Issues with the Embedded C SDK

## Retry Policies

### 1. How to set up a retry mechanism for using azure-sdk-for-c IoT?
 
Please refer to the guidelines for implementing a retry logic documented in the
<a href='https://github.com/Azure/azure-sdk-for-c/blob/master/sdk/docs/iot/mqtt_state_machine.md#retrying-operations'>MQTT state machine</a>:

It is highly recommended to have the reconnection strategy based on the retry logic detailed in the documentation above.

Not having a controlled retry strategy may actually lead to increased delays or preventing the client from effectively reconnecting to the Azure IoT Hub (due to timing or throttling).
	 
### 2.  How to tweak the retry logic frequency?
 
According to the <a href='https://github.com/Azure/azure-sdk-for-c/blob/master/sdk/docs/iot/mqtt_state_machine.md#retrying-operations'>documentation</a>, the following arguments control the frequency of the retry logic:
	 
* min_retry_delay_msec = 1000;
* max_retry_delay_msec = 100000;
* max_random_msec = 5000;

Note that az_iot_retry_calc_delay(...) is based on an Exponential Backoff with Jitter strategy.
 

To make the retry attempts to be more sparse from the beginning, increase the value of `min_retry_delay_msec`.

To reduce the maximum delay between attempts, decrease the value of `max_retry_delay_msec`.

To increase the variability (jitter) between successive retry attempts, increase the value of `max_random_msec`.
 
 
## Sequence of API calls
 
Please refer to the <a href='https://github.com/Azure/azure-sdk-for-c/blob/master/sdk/docs/iot/mqtt_state_machine.md'>guidelines</a>. The minimum set of functionality needed to connect to the Azure IoT Hub and exchange messages is to:
 
1. Establish a secure socket connection with the Azure IoT Hub;

	This includes the following concepts:
	* Connect to the port where the Azure IoT Hub listens for MQTT connections (8883, or 443 if using MQTT over WebSockets) - <a href='https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-protocols'>reference</a>
	
	* Encrypt the connection using a SSL API (example: OpenSSL) and the highest TLS version supported (currently TLS 1.2) - <a href='https://docs.microsoft.com/azure/iot-hub/iot-hub-tls-support'>reference</a>
	
	*	Validate the server certificate using the proper root certificate.
	Baltimore CyberTrust Root - <a href='https://www.digicert.com/digicert-root-certificates.htm'>reference</a>
 
2. Connect a MQTT client to the Azure IoT Hub, providing proper authentication information;
* The Azure SDK for Embedded C IoT client must be initialized using `az_iot_hub_client_init`.
 
*	Authentication schemes:

*	If using x509 certs for device authentication
	* Client certificate must be set on the TLS layer to be presented to the Azure IoT Hub.
	* MQTT client must use username obtained with `az_iot_hub_client_get_user_name` and empty (NULL) password: <a href='https://github.com/Azure/azure-sdk-for-c/blob/master/sdk/samples/iot/hub/src/paho_iot_hub_telemetry_example.c'>Example</a>
 
* If using SAS tokens:
	* MQTT client must use username obtained with `az_iot_hub_client_get_user_name` and password obtained with `az_iot_hub_client_sas_get_signature` and `az_iot_hub_client_sas_get_password`: <a href='https://github.com/Azure/azure-sdk-for-c/blob/master/sdk/samples/iot/hub/src/paho_iot_hub_sas_telemetry_example.c'>Example</a>
 
3. Subscribe to the topics expected by the Azure IoT Hub for the features if supports;
Use the following macros or functions to provide the topics the MQTT client must subscribe to to use the features supported by Azure IoT Hub:
	* AZ_IOT_HUB_CLIENT_C2D_SUBSCRIBE_TOPIC
	* AZ_IOT_HUB_CLIENT_METHODS_SUBSCRIBE_TOPIC
	* AZ_IOT_HUB_CLIENT_TWIN_RESPONSE_SUBSCRIBE_TOPIC
	* AZ_IOT_HUB_CLIENT_TWIN_PATCH_SUBSCRIBE_TOPIC
	
	Please refer to the header for more <a href='https://github.com/Azure/azure-sdk-for-c/blob/master/sdk/inc/azure/iot/az_iot_hub_client.h'>Documentation</a>.
	
4. Parse messages received from the Azure IoT Hub;

	Messages sent by the Azure IoT Hub for the features supported have specific topic names, which contains the key information of each response.

	The following functions shall be used to parse the relevant information from the topic names for each feature:

	* az_iot_hub_client_c2d_parse_received_topic
	* az_iot_hub_client_methods_parse_received_topic
	* az_iot_hub_client_twin_parse_received_topic
	
	Please refer to the header for more <a href='https://github.com/Azure/azure-sdk-for-c/blob/master/sdk/inc/azure/iot/az_iot_hub_client.h'>Documentation</a>.
 
5. Publish messages to the topics expected by the Azure IoT Hub for the features if supports;
Use the following functions to provide the topics the MQTT client must publish to to use the features supported by Azure IoT Hub:
 
	* az_iot_hub_client_telemetry_get_publish_topic
	* az_iot_hub_client_methods_response_get_publish_topic
	* az_iot_hub_client_twin_document_get_publish_topic
	* az_iot_hub_client_twin_patch_get_publish_topic

	Please refer to the header for more <a href='https://github.com/Azure/azure-sdk-for-c/blob/master/sdk/inc/azure/iot/az_iot_hub_client.h'>Documentation</a>.
 
## Can't get my TLS to work
 
## 1. Issue found in one of our samples
 
If the customer has used one of our samples as a base to develop their application (against the same stacks and APIs used by the samples), the customer must refer to all the proper calls in those samples to ensure their system can connect and work properly with the Azure IoT Hub.

Locations of our samples:
* <a href='https://github.com/Azure/azure-sdk-for-c/tree/master/sdk/samples/iot/hub'>Hub samples</a>
* <a href='https://github.com/Azure/azure-sdk-for-c/tree/master/sdk/samples/iot/provisioning'>Device Provisioning samples</a>

Samples also have detailed step-by-step guides. Please explore more <a href='https://github.com/Azure/azure-sdk-for-c/tree/master/sdk/samples/iot/hub#azure-iot-hub-samples'>here</a>
	 
## 2. Issue not found in one of our samples
 
In cases where the customer code is not directly based on any of the samples we do provide, the customer must consult with the developer of TLS/socket layers for guidance (e.g., WolfSSL, OpenSSL, etc).

All the basic requirements of the Azure IoT Hub for socket security will apply to any SSL API used.

Resources available:
* <a href='https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-connectivity'>https://docs.microsoft.com/azure/iot-hub/iot-hub-troubleshoot-connectivity</a>
* <a href='https://azure.microsoft.com/blog/azure-iot-hub-server-tls-leaf-certificate-renewal-may-2017/'>https://azure.microsoft.com/blog/azure-iot-hub-server-tls-leaf-certificate-renewal-may-2017/</a>


