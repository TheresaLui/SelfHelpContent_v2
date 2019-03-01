<properties
	pageTitle="Troubleshooting On-demand Assessments"
	description="OMS On-demand Assessments Troubleshooting Self Help and Explanation"
	infoBubbleText=""
	service="microsoft.operationalinsights"
	resource="operationalinsightsaccounts"
	authors="v-dinova"
	authoralias="v-dinova"
	displayOrder=""
	articleId="operationalinsights-troubleshooting-the-onboarding-process"
	diagnosticScenario=""
	selfHelpType="generic"
supportTopicIds="32612423"
	resourceTags="assessments,on-boarding,troubleshooting"
	productPesIds="15725"
	cloudEnvironments="public"
/>

# Troubleshooting On-Demand Assessments

If you are having issues with On-Demand Assessments, please see the documentation below.

## **Recommended Documents**

[Troubleshooting the On-demand Assessments](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting)<br>
This document describes the most common problems experienced with On-Demand Assessments and how to try to solve them. Click on the link that best describes your problem:<br>
 - [Microsoft Monitoring Agent (MMA) Installation issues](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#microsoft-monitoring-agent-mma-installation-issues)
   * [Cannot successfully link to the specified workspace as part of the MMA installation](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#cannot-successfully-link-to-the-specified-workspace-as-part-of-the-mma-installation)
 - [Learn more about Linking and Permissions](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#linking-and-permissions)
 - [Add-*AssessmentTask Commandlet related issues](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#add-assessmenttask-commandlet-related-issues)
   * [Windows Server 2008 R2 does not recognize Add-*AssessmentTask commandlets](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#windows-server-2008-r2-does-not-recognize-add-assessmenttask-commandlets)
   * [On any platform, if the Add-*AssessmentTask commandlets are not recognized](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#on-any-platform-if-the-add-assessmenttask-commandlets-are-not-recognized)
   * [Troubleshooting Assessment Installation Errors when executing an Add-*AssessmentTask cmdlet](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#troubleshooting-assessment-installation-errors-when-executing-an-add-assessmenttask-cmdlet)
 - [Requirements for successfully running the scheduled task](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#requirements-for-successfully-running-the-scheduled-task)
   * [Verify the user account Group Policies: Logon as Batch Job Permission](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#verify-the-user-account-group-policies-logon-as-batch-job-permission)
   * [Do not forcefully unload the user registry at user logoff](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#do-not-forcefully-unload-the-user-registry-at-user-logoff)
   * [Disable the FIPS Policy](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#disable-the-fips-policy)
   * [Network Access: Do not allow storage of passwords and credentials](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#network-access-do-not-allow-storage-of-passwords-and-credentials)
   * [Assessment has not been added to your workspace](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#assessment-has-not-been-added-to-your-workspace)
 - [Assessment Task Running Issues: Inactive / No Data found in Azure Log Analytics](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#inactive--no-data-found-in-azure-log-analytics)
    * [Verify Log Analytics Agent connectivity](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#verify-log-analytics-agent-connectivity)
    * [Look at the Heartbeat messages from the AgentHealthAssessment solution](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#look-at-the-heartbeat-messages-from-the-agenthealthassessment-solution)
 - [Assessment Task Running Issues: Data from OnDemand assessment is no longer seen in Log Analytics, but it was seen in the past](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#data-from-ondemand-assessment-is-no-longer-seen-in-log-analytics-but-it-was-seen-in-the-past)
   * [Restart healthservice if data files are pending ingestion](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#restart-healthservice-if-data-files-are-pending-ingestion)
   * [Check for any conflicting omsassessment.exe processes running](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#check-for-any-conflicting-omsassessmentexe-processes-running)
   * [Go through error in the discovery log file](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#go-through-error-in-the-discovery-log-file)
   * [Large file ingestion](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#large-file-ingestion)
   * [Try to reduce the number of targets per assessment schedule](https://docs.microsoft.com/en-us/services-hub/health/assessments-troubleshooting#try-to-reduce-the-number-of-targets-per-assessment-schedule)
   * [Go through Scheduled Task dispatch and uploader log files](https://docs.microsoft.com/en-us/services-hub/health/assessments-troubleshooting#go-through-scheduled-task-dispatch-and-uploader-log-files)
