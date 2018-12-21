<properties
	pageTitle="Troubleshooting the On-demand Assessments"
	description="OMS On-demand Assessments Troubleshooting Self Help and Explanation"
	infoBubbleText=""
	service="microsoft.assessments"
	resource="recommendations"
	authors="v-dinova"
	authoralias="v-dinova"
	displayOrder=""
	articleId="microsoftassessments-troubleshooting-the-onboarding-process"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32612415,32612423,32612431,32612459,32612494,32612522,32612528"
	resourceTags="assessments,on-boarding,troubleshooting`"
	productPesIds="15725"
	cloudEnvironments="public"
/>

# Troubleshooting the On-demand Assessments

## **Recommended steps**


The below steps would walk you through from start to end and make you verify the
correctness of each requirements that are to be met in running the On-Demand
Assessments:

The most common issues we see users encounter are: (Guidance on how to resolve
them is mentioned below in the article)

1.  The user account is not part of the Local Administrator group on the data
    collection machine from where the assessment is running.

2.  When you ran the assessment but see no data in Log Analytics -\> Restart
    healthservice if data files are pending ingestion.

3.  Error message: "You dont have access to Azure Log Analytics" in Services Hub
    -\> Health -\> Assessments.

**Linking and Permissions**

1.  [Watch the
    video](https://video.serviceshub.microsoft.com/PublicPage/video/5581.aspx) to
    pre-configure your on-demand assessments.

2.  [Verify that you have the Azure Subscription Owner role on the Azure
    Subscription](https://docs.microsoft.com/services-hub/health/health-kb-adduserazure) on
    the same email id that you use to login into Services Hub.

3.  You should be able to see the below page in Services Hub -\> Health -\>
    Assessments upon successful linking.

4.  Confirm that the Log Analytics workspace you have access to is the one that
    is linked in Services Hub. If not ask them to re-link by clicking on profile
    at the top right -\> Edit Log Analytics Workspace and link the desired
    workspace.

5.  Confirm that you have added the desired assessment from the catalog. 

**Verify the user account Group Policies**

**Local Administrator Rights**

To begin,

1.  The user account setting up the assessment must be a Local Administrator.

2.  Go to the Start menu (in the lower left corner of your Windows desktop).

3.  Select Settings then Control Panel (depending on which version of Windows
    you have).

4.  Open User Accounts.

5.  Choose the Users tab.

If Administrator is displayed in the Group column or for your user name, it
means you have administrative privileges. If you don't have administrator
access, ask your network administrator to give you administrator privileges, or
ask your network administrator to log in to your system as an administrator.

**Logon as Batch Job Permission**

Please Note: At times the assessment may not get triggered from the task
scheduler. This may happen if the user does not have running batch job
permission. If that’s the case, this permission needs to be explicitly granted
by going in here from gpedit.msc

Computer Configuration\\Windows Settings\\Security Settings\\Local
Policies\\User Rights Assignment

1.  Right click on "Log on as batch job" and select Properties.

2.  Click "Add User or Group", and include the relevant user.

**Do not forcefully unload the user registry at user logoff**

On the data collection machine, change the following setting in the group policy
editor (gpedit.msc) from "not configured" to "enabled": Computer
Configuration-\>Administrative Templates -\> System -\> User Profiles

'Do not forcefully unload the user registry at user logoff'

**Disable the FIPS Policy**

1.  In Control Panel, click Administrative Tools, and then double-click Local
    Security Policy.

2.  In Security Settings, expand Local Policies, and then click Security
    Options. 

3.  Under Policy in the right pane, double-click System cryptography: Use FIPS
    compliant algorithms for encryption, hashing, and signing, and then click
    Disabled

**Network Access: Do not allow storage of passwords and credentials**

1.  This error occurs with the message "A specified logon session does not
    exist. It may already have been terminated"

2.  To resolve this, go to: SECPOL.MSC \| Security Settings \| Local Policies \|
    Security Options

3.  Network access: Do not allow storage of passwords and credentials for
    network authentication 

4.  Set the policy to disabled

**Inactive / No Data found in Azure Log Analytics**

**Verify Log Analytics Agent connectivity**

To ensure that the agent can communicate with OMS, go to: Control Panel,
Security & Settings, Microsoft Monitoring Agent. Under the Azure Log Analytics
(OMS) tab, look for a green check mark.

A green check mark icon confirms that the agent is able to communicate with the
Azure service.

A yellow warning icon means the agent is having issues communication with Log
Analytics.

One common reason is the Microsoft Monitoring Agent service has stopped. Use
service control manager to restart the service.

If you have a firewall restriction in place, make sure the below ports are
opened up:

-   mms.microsoft.com, Log Analytics portal

-   workspaceId.ods.opinsights.azure.com, [Data Collector
    API](https://docs.microsoft.com/azure/azure-monitor/platform/data-collector-api)

-   \*.ods.opinsights.azure.com, Agent communication - configuring [firewall
    settings](https://docs.microsoft.com/azure/azure-monitor/platform/agent-windows)

-   \*.oms.opinsights.azure.com, Agent communication - configuring [firewall
    settings](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-windows)

-   \*.blob.core.windows.net, Agent communication - configuring [firewall
    settings](https://docs.microsoft.com/azure/log-analytics/log-analytics-agent-windows)

**Restart healthservice if data files are pending ingestion**

Please close all active powershell windows on the machine. Now, if you check the
working directory of the Assessment and find the files with names like
new.recommendations.\*\*\* (see screenshot below):

Open Command Prompt in Administrator mode and type in the below: net stop
healthservice net start healthservice

After running the below command, the files would change to be processed as shown
below which means the files have been ingested successfully and data should be
visible on Log Analytics in about 30 min.

**Check for any conflicting omsassessment.exe processes running**

Open up Task Manager and look for a process named as omsassessment.exe. If found
it indicates that the assessment is still running.

If it has been quite long (for eg, if you find this process has been running for
over a day), it is possible that the assessment agent could not process data. So
please proceed to the next troubleshooting steps below.

**Go through any errors in the prerequisite file**

Go to the assessment working directory and look at the pre-requisites
(processed.prerequisites) files to find any errors mentioned for the assessment
targets.

If any errors are found, for example WMI connectivity issues, the target names
and the error would be mentioned in this file. Please resolve this and then
trigger the assessment from the Task Scheduler

Task Scheduler -\> Microsoft -\> Operations Management Suite -\> AOI\*\*\*\*\*
-\> Assessments and right click and hit run on the desired assessment scheduled
task

**Go through error in the discovery log file**

Go to the assessment working directory and go into the 6-8 digit numbered folder
inside the directory. Look for a folder called as Logs within which you will
find a file named as DiscoveryTrace\*\*\*

Look for any errors or exceptions in this file and resolve them since they would
be related to credential/permissions issue, WMI failure, network issue etc.

**Large file ingestion**

If the below files processed.recommendations.\*\*\* size is greater than 250MB,
the files might be difficult to be processed by the Log Analytics Agent. If you
encounter this scenario and are not able to see the data in Log Analytics please
contact serviceshubteam\@ppas.uservoice.com and let us know about your issue.

**Try to reduce the number of targets per assessment schedule**

If you are running the Windows Server, Windows Client or SQL Assessment and have
added more than 5 targets in a single scheduled task, sometimes its possible
that the assessment agent would not be able to process so many targets in one
go. If you encounter this scenario, please use the below cmdlet to remove any
existing configuration:

Remove-WindowsClientAssessmentTask Remove-WindowsServerAssessmentTask
Remove-SQLAssessmentTask

Now run the Add-AssessmentTasks again with fewer targets. You can add multiple
such tasks and create batches of tasks with 3-5 targets per task which would
result in a quicker evaluation of your entire environment.
