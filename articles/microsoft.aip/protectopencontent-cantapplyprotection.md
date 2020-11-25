<properties
  pagetitle="Azure Information Protection client - Unable to apply a protection label&#xD;"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel"
  selfhelptype="Generic"
  supporttopicids="32727972"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="protectopencontent_cantapplyprotection"
  ownershipid="AzureIdentity_InformationProtection" />
# Unable to apply a protection label in Azure Information Protection client

## **Recommended Steps**

1. If you created a new label that applies protection, it can take up to 24 hours for a computer running the Azure Information Protection client to get the changed settings.
2. If you waited 24 hours and still can't apply this label, select **Help and feedback** from the **Protect/Sensitivity** button on the Office ribbon, then **Reset settings**. This action signs out the user, deletes the currently downloaded Azure Information Protection policy, and resets the user settings for the Azure Rights Management Service (RMS).
3. If you have never used Azure Information Protection before, verify that your OnBoarding policy is set correctly:

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
	
	* For more information about RMS OnBoarding policy, see [Set-AadrmOnboardingControlPolicy](https://docs.microsoft.com/powershell/module/aadrm/set-aadrmonboardingcontrolpolicy?view=azureipps)

4. Verify that you are trying to apply a label for a supported file type and that the file is not password protected. See [File types supported by the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-file-types#files-that-cannot-be-protected-by-default).
5. If you are installing on Office 2010, make sure that you have defined the ServiceLocation parameter [as shown here](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-install#to-install-the-azure-information-protection-client-by-using-the-executable-installer)
6. Azure Information Protection does not support having multiple versions of Office installed or multiple users signed in to Office. Log out all users from Office and try again. See [requirements](https://docs.microsoft.com/azure/information-protection/requirements#applications)
7. If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect** or **Sensitivity** button, and **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your local disk, and then attach them to the service request

## **Recommended Documents**

* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
