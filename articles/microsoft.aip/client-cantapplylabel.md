<properties
	pageTitle="Azure Information Client - Can't apply this label error"
	description="Azure Information Client - Can't apply this label error"
	service="microsoft.aip"
	resource="aip"
	authors="nihendle"
	ms.author="nihendle, orbarak"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32584334"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="a2e21818-3554-4ea5-bde3-5a02a3241ada"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection client - can't apply this label error

## **Recommended Steps**

1. If you created a new label that applies protection, it can take up to 15 minutes for a computer running the Azure Information Protection client to get these changed settings. Behind the scenes, this configuration creates a [protection template](https://docs.microsoft.com/azure/information-protection/deploy-use/refresh-templates).
2. If you wait 15 minutes and still can't apply this label, select **Reset Settings** from the **Protect** button on the Office ribbon, then **Help and feedback**. This action signs out the user, deletes the currently downloaded Azure Information Protection policy, and resets the user settings for the Azure Rights Management service.
3. If you have never used AIP before, please verify your OnBoarding policy is set correctly:

	* Open a PowerShell session as administration and run the below commands:
	
	```
	Install-Module -Name AADRM
	Connect-AadrmService 
	Get-AadrmOnboardingControlPolicy | fl 
	```
	
	* The output will contain 3 lines:
	
	```
	UseRmsUserLicense     : False
	SecurityGroupObjectId :
	Scope                 : All
	```
	
	* If you have a value defined under SecurityGroupObjectId, it means you need to add your user to the group shows in that field in order to use RMS
	
	* More information about RMS OnBoarding policy can be found here: [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps)

4. Verify that you are trying to apply label for a supported file type and that the file is not password protected: [File types supported by the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-file-types#files-that-cannot-be-protected-by-default)
5. If you are installing on Office 2010, make sure you have defined ServiceLocation parameter [as shown here](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-install#to-install-the-azure-information-protection-client-by-using-the-executable-installer)
6. Azure Information Protection does not support having multiple version of Office installed and multiple users signed in to Office. Try to logout all users logged into Office and try again [More information](https://docs.microsoft.com/azure/information-protection/requirements#applications)
7. The Azure Information Protection clients do not support multiple versions of Office on the same computer. These clients also do not support switching user accounts in Office
8. If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect** button -> **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
