<properties
	pageTitle="I configured Windows 10 update settings in the Intune classic portal. Should I migrate them to Intune in the Azure portal?"
	description="I configured Windows 10 update settings in the Intune classic portal. Should I migrate them to Intune in the Azure portal?"
	service="microsoft.intune"
	resource="intune"
	authors="mackie1604"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="software_updates_selfhelp"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="4cb76acf-10e1-4987-afd9-e390404bd5aa"
	ownershipId="IntuneCxP_Intune"
/>

# I configured Windows 10 update settings in the Intune classic portal. Should I migrate them to Intune in the Azure portal?

## **Recommended steps**

To avoid conflicts, delete your update settings in the classic portal and recreate them in the Azure portal.

  1.  Go to the Azure portal and click **All Services**.
  2.  In the **Filter** field, type **Intune**. In the results, click **Microsoft Intune**.  
  3.  Click **Software updates > Windows 10 Update Rings > Create**. 
  4.  Enter a name, description, and click **Configure**. 
  5.  Configure your organizations software update settings.
  6.  Select **OK**.
  7.  In **Create Update Ring**, select **Create**. 

For additional details about the settings covered in these steps, see the article [Manage software updates in Intune.](https://docs.microsoft.com/intune/windows-update-for-business-configure)

