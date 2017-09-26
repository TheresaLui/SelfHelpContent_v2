<properties
	pageTitle="Issues with the gateway certificate"
	description="How to resolve issues with the gateway certificate"
	service="microsoft.servermanagement"
	resource="gateways"
	authors="samli"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, MoonCake"
/>

# Issues with the gateway certificate

## **Recommended steps**
Certificate requirements may change, or certificates may expire. To resolve, try one of the following solutions:

* Use the gateway installer to register a new certificate. Previously saved credentials will need to be re-entered.
  1. On the gateway machine, go to “Programs and Features” and uninstall “Server management tools gateway”.
  2. [Generate a new gateway deployment package](data-blade:Microsoft_Azure_RSMT.GatewaySetupBlade), download and install it on the gateway machine. During the install, choose either a new self-signed certificate or an existing installed certificate.
  3. If you had saved credentials for your connections, you can use Manage As to enter the credentials again since the new certificate cannot decrypt previously saved credentials.
* Use the certificate rotation script to register a new certificate. Previously saved credentials will continue to work.
  1. On the gateway machine, open PowerShell with Administrator privileges.
  2. Change directory to the Scripts folder where the gateway software is installed, e.g. `C:\Program Files\ServerManagementToolsGateway\Scripts`
  3. Run the `New-GatewayEncryptionCert.ps1` with no parameters to generate a new self-signed certificate, or with the `-Thumbprint <thumbprint>` parameter to use an existing installed certificate.
  4. Restart the gateway service. If you had saved credentials for your connections, they will continue to work if you access the connections at least once during the certificate rotation period (currently 30 days), which allows the previously saved credentials to be re-encrypted using the new certificate.
