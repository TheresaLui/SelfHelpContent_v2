<properties
	pageTitle="Manage Software Updates - Windows 10 Update Rings"
	description="Manage Software Updates - Windows 10 Update Rings"
	service="microsoft.intune"
	resource="intune"
	authors="rciliax"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32599685"
	resourceTags=""
	productPesIds="15584"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="153005d9-c1e9-47ff-8e75-e7516b318b06"
	ownershipId="IntuneCxP_Intune"
/>

# Manage Software Updates - Windows 10 Update Rings

## **Recommended steps**

Let's take a look at a few common issues with Windows 10 update rings and how to resolve them:

**I configured software updates through a Windows 10 update ring, but the updates are not being deployed.**

* Consider changing Windows servicing from a **Semi-Annual Channel** release type to a stricter, more frequent release type. 

* Check the deferral period for **Quality update** and **Feature update**. The deferral period could lead to delay in updates for up 180 days. For more information on these settings see [Manage software updates in Intune.](https://docs.microsoft.com/intune/windows-update-for-business-configure)

**I configured Windows 10 update settings in the Intune classic portal. Should I migrate them to Intune in the Azure portal?**

To avoid conflicts, delete your update settings in the classic portal and recreate them in the Azure portal.

  1.  Go to the Azure portal and click **All Services**.
  2.  In the **Filter** field, type **Intune**. In the results, click **Microsoft Intune**.  
  3.  Click **Software updates > Windows 10 Update Rings > Create**. 
  4.  Enter a name, description, and click **Configure**. 
  5.  Configure your organizations software update settings.
  6.  Select **OK**.
  7.  In **Create Update Ring**, select **Create**. 

For additional details about the settings covered in these steps, see the article [Manage software updates in Intune.](https://docs.microsoft.com/intune/windows-update-for-business-configure)

**The PCs in my organization are downloading updates individually. Is there a way they can download and then share updates?**

Yes, Delivery Optimizations download mode setting enables sharing between multiple PCs. Available download modes include:

  * HTTP Only
  * LAN
  * Group
  * Internet
  * Simple
  * Bypass

To configure Delivery Optimization see [Configure Delivery Optimization for Windows 10 updates.](https://docs.microsoft.com/windows/deployment/update/waas-delivery-optimization)

**I want to defer the Windows 10 updates that are being pushed to users.**

  1.  Sign in to the Azure portal.
  2.  Select **Software updates > Windows 10 Update Rings**.
  3.  If you do not already have an update ring, click to create a new one. 
  4.  Enter a name and optional description. Then click **Settings Configure**.
  5.  Customize the timeframe for deferring different types of updates. Maximum deferred time is based on the type of update.  
    * **Quality updates** can be deferred up to 30 days from their release.
    * **Feature updates** can be deferred up to 180 days from their release.

For more information about managing software updates, see the article [Manage software updates.](https://docs.microsoft.com/intune/windows-update-for-business-configure)

**My devices installed their scheduled updates, even though I issued a pause command.**

When a pause command is issued, devices do not process the command until the next time they check in to Intune. Because of this, your devices may have:

  * Installed the scheduled updates prior to check-in.
  * Been powered off when you issued the pause command. In this case, when the devices were powered on, they may have downloaded and installed the scheduled updates prior to check-in.

## **Recommended documents**

[Manage software updates](https://docs.microsoft.com/intune/windows-update-for-business-configure)<br>
[Review Intune TechNet to find answers and solutions to common issues](https://aka.ms/intuneforums)<br>
[Check out Service Health to see current status of the service](https://portal.office.com/AdminPortal/Home#/MessageCenter)<br>
