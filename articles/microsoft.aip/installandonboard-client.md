<properties
	pageTitle="Azure Information Client - Installing, Onboarding, or Decommissioning - AIP Client Installation"
	description="Azure Information Client - Installing, Onboarding, or Decommissioning - AIP Client Installation"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32727932"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
	articleId="MIP_Onboard_Client_Install"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection client - Installing, Onboarding, or Decommissioning - AIP Client Installation

## **Recommended Steps**

1. Download the Azure Information Protection client from the [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53018).

2. Review the following documentation for installation instructions:

	- For end users: [Download and install the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/rms-client/install-unifiedlabelingclient-app)
	- For administrators: [Install the Azure Information Protection client for users](https://docs.microsoft.com/azure/information-protection/rms-client/clientv2-admin-guide-install)

3. If you have encountered an error during the installation process, follow the guidelines at [Fix problems that block programs from being installed or removed](https://support.microsoft.com/help/17588/windows-fix-problems-that-block-programs-being-installed-or-removed).

4. If you still encounter problems installing the client itself after running the tool listed above, locate the `%temp%` folder and provide the client installation log files that start with `Microsoft_Azure_Information_Protection_XXXXXXXXXX.log`.

5. If the installation succeeded and you are experiencing issues using Azure Information Protection, please select the appropriate Support Topic for relevant solutions.

6. If your issue is related to the Azure Information Protection scanner, select the appropriate support topic.

7. If you are missing the Sensitivity labels in Excel only, and your client appears to work offline, make sure to remove any files in the following folders: 

    ```
    C:\Users\<UserName>\AppData\Roaming\Microsoft\Excel\XLSTART
    C:\Program Files\Microsoft Office\Root\Office16\XLSTART 
    ```

    and add the following Registry key:

    ```
    [HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\Common\Security\Labels]
    "UseOfficeForLabelling"=dword:00000000
    ```

8. If you believe your issue is still relevant to installation issues, even if Azure Information Protection was successfully installed, please export AIP logs using the method described below.

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook.
2. Select the **Sensitivity** or **Protect** button -> **Help and feedback**.
3. Select **Export Logs**.
4. Save the logs to a location of your choice and then attach them to this service request.

## **Recommended Documents**

* [Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quickstart: Deploy the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/quickstart-deploy-client)<br>
* [Download the Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
