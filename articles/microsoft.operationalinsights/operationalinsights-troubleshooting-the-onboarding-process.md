<properties
	pageTitle="Troubleshooting Health Check and On-Demand Assessments"
	description="OMS Health Check and On-demand Assessments Troubleshooting Self Help and Explanation"
	infoBubbleText=""
	service="microsoft.operationalinsights"
	resource="operationalinsightsaccounts"
	authors="v-dinova"
	ms.author="v-dinova"
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
#  Troubleshooting Health Check and On-Demand Assessments  #

Health Checks are free Log Analytics offerings. OnDemand Assessment are premium offerings on top of Log Analytics available to Microsoft Premier and Unified customers. If you are interested in purchasing OnDemand Assessments to get a more comprehensive set of rules and analysis, contact InterestedInODA@microsoft.com

## **Recommended documents**

If you are having issues with On-Demand Assessments, please see the documentation below.

### **Troubleshooting On-Demand Assessments**

[Office 365 solutions unavailable in US Government Cloud (Fairfax) and China Government Cloud Log Analytics](https://docs.microsoft.com/services-hub/health/fairfax-o365-solutions-unavailable)

This document provides information about the progress of implementing and deploying of the Office 365 solutions to government clouds and the currently estimated time when these will start to be supported

[Troubleshooting the On-demand Assessments](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting)

This document describes the most common problems experienced with On-Demand Assessments and how to try to solve them. Click on the link that best describes your problem:

 - [Microsoft Monitoring Agent (MMA) Installation issues](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#microsoft-monitoring-agent-mma-installation-issues)
   - [Cannot successfully link to the specified workspace as part of the MMA installation](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#cannot-successfully-link-to-the-specified-workspace-as-part-of-the-mma-installation)
 - [Learn more about Linking and Permissions](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#linking-and-permissions)
 - [Add-*AssessmentTask Commandlet related issues](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#add-assessmenttask-commandlet-related-issues)
   - [Windows Server 2008 R2 does not recognize Add-*AssessmentTask commandlets](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#windows-server-2008-r2-does-not-recognize-add-assessmenttask-commandlets)
   - [On any platform, if the Add-*AssessmentTask commandlets are not recognized](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#on-any-platform-if-the-add-assessmenttask-commandlets-are-not-recognized)
   - [Troubleshooting Assessment Installation Errors when executing an Add-*AssessmentTask cmdlet](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#troubleshooting-assessment-installation-errors-when-executing-an-add-assessmenttask-cmdlet)
 - [Requirements for successfully running the scheduled task](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#requirements-for-successfully-running-the-scheduled-task)
   - [Verify the user account Group Policies: Logon as Batch Job Permission](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#verify-the-user-account-group-policies-logon-as-batch-job-permission)
   - [Do not forcefully unload the user registry at user logoff](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#do-not-forcefully-unload-the-user-registry-at-user-logoff)
   - [Disable the FIPS Policy](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#disable-the-fips-policy)
   - [Network Access: Do not allow storage of passwords and credentials](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#network-access-do-not-allow-storage-of-passwords-and-credentials)
   - [Assessment has not been added to your workspace](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#assessment-has-not-been-added-to-your-workspace)
 - [Assessment Task Running Issues](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#inactive--no-data-found-in-azure-log-analytics)
    - [Verify Log Analytics Agent connectivity](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#verify-log-analytics-agent-connectivity)
    - [Look at the Heartbeat messages from the AgentHealthAssessment solution](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#look-at-the-heartbeat-messages-from-the-agenthealthassessment-solution)
   * [Data from OnDemand assessment is no longer seen in Log Analytics, but it was seen in the past](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#data-from-ondemand-assessment-is-no-longer-seen-in-log-analytics-but-it-was-seen-in-the-past)
   - [Restart healthservice if data files are pending ingestion](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#restart-healthservice-if-data-files-are-pending-ingestion)
   - [Check for any conflicting omsassessment.exe processes running](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#check-for-any-conflicting-omsassessmentexe-processes-running)
   - [Go through error in the discovery log file](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#go-through-error-in-the-discovery-log-file)
   - [Large file ingestion](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#large-file-ingestion)
   - [Try to reduce the number of targets per assessment schedule](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#try-to-reduce-the-number-of-targets-per-assessment-schedule)
   - [Go through Scheduled Task dispatch and uploader log files](https://docs.microsoft.com/services-hub/health/assessments-troubleshooting#go-through-scheduled-task-dispatch-and-uploader-log-files)


## **Troubleshooting Health Check**

If you are having issues with Health Check, please see the documentation below.

### **Recommended documents**

#### AD Health Check   

[Optimize your Active Directory environment with the Active Directory Health Check solution in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment)  

This document provides guidance both on installing the solution and taking corrective actions for potential problems.

 - [Prerequisites](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#prerequisites)
 - [Active Directory Health Check data collection details](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#active-directory-health-check-data-collection-details)
 - [Understanding how recommendations are prioritized](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#understanding-how-recommendations-are-prioritized)
   - [How weights are calculated](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#how-weights-are-calculated)
   - [Focus areas](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#focus-areas)
   - [Should you aim to score 100% in every focus area?](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#should-you-aim-to-score-100-in-every-focus-area)
 - [Use health check focus area recommendations](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#use-health-check-focus-area-recommendations)
   - [View recommendations for a focus area and take corrective action](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#to-view-recommendations-for-a-focus-area-and-take-corrective-action)
 - [Ignore recommendations](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#ignore-recommendations)
   - [Identify recommendations that you will ignore](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#to-identify-recommendations-that-you-will-ignore)
   - [Create and use an IgnoreRecommendations.txt text file](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#to-create-and-use-an-ignorerecommendationstxt-text-file)
   - [Verify that recommendations are ignored](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#to-verify-that-recommendations-are-ignored)
 - [AD Health Check solutions FAQ](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#ad-health-check-solutions-faq)
 - [Additional help](https://docs.microsoft.com/azure/azure-monitor/insights/ad-assessment#next-steps)


#### SCOM Health Check

[Optimize your environment with the System Center Operations Manager Health Check (Preview) solution](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment)

This document provides guidance on installing and configuring the solution, and taking corrective actions for potential problems.

- [Installing and configuring the solution](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#installing-and-configuring-the-solution)
- [System Center Operations Manager Health Check data collection details](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#system-center-operations-manager-health-check-data-collection-details)
- [Operations Manager run-as accounts for Log Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#operations-manager-run-as-accounts-for-log-analytics)
   - [Set the Run As account](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#set-the-run-as-account)
   - [SQL script to grant granular permissions to the Run As account](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#sql-script-to-grant-granular-permissions-to-the-run-as-account)
   - [Configure the health check rule](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#configure-the-health-check-rule)
   - [Enable the rule for a specific management server](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#enable-the-rule-for-a-specific-management-server)
   - [Configure the run frequency](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#configure-the-run-frequency)

- [Understanding how recommendations are prioritized](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#understanding-how-recommendations-are-prioritized)
   - [How weights are calculated](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#how-weights-are-calculated)
   - [Focus areas](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#focus-areas)
   - [Should you aim to score 100% in every focus area?](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#should-you-aim-to-score-100-in-every-focus-area)

- [Use health check focus area recommendations](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#use-health-check-focus-area-recommendations)
   - [View recommendations for a focus area and take corrective action](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#to-view-recommendations-for-a-focus-area-and-take-corrective-action)

- [Ignore recommendations](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#ignore-recommendations)
   - [Identify recommendations that you want to ignore](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#to-identify-recommendations-that-you-want-to-ignore)
   - [Create and use an IgnoreRecommendations.txt text file](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#to-create-and-use-an-ignorerecommendationstxt-text-file)
   - [Verify that recommendations are ignored](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#to-verify-that-recommendations-are-ignored)

- [System Center Operations Manager Health Check solution FAQ](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#system-center-operations-manager-health-check-solution-faq)
- [Additional help](https://docs.microsoft.com/azure/azure-monitor/insights/scom-assessment#next-steps)
 

#### SQL Health Check

[Optimize your SQL environment with the SQL Server Health Check solution in Log Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment)

This document provides guidance both on installing the solution and taking corrective actions for potential problems.

 - [Prerequisites](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#prerequisites)
 - [SQL Health Check data collection details](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#sql-health-check-data-collection-details)
 - [Operations Manager run-as accounts for Log Analytics](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#operations-manager-run-as-accounts-for-log-analytics)
   - [Set the Run As account for SQL Health Check](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#set-the-run-as-account-for-sql-health-check)
   - [Configure the SQL Run As account using Windows PowerShell](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#to-configure-the-sql-run-as-account-using-windows-powershell)
 - [Understanding how recommendations are prioritized](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#understanding-how-recommendations-are-prioritized)
   - [How weights are calculated](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#how-weights-are-calculated)
   - [Focus areas](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#focus-areas)
   - [Should you aim to score 100% in every focus area?](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#should-you-aim-to-score-100-in-every-focus-area)
 - [Use Health Check focus area recommendations](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#use-health-check-focus-area-recommendations)
   - [View recommendations for a focus area and take corrective action](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#to-view-recommendations-for-a-focus-area-and-take-corrective-action)
 - [Ignore recommendations](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#ignore-recommendations)
   - [Identify recommendations that you will ignore](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#to-identify-recommendations-that-you-will-ignore)
   - [Create and use an IgnoreRecommendations.txt text file](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#to-create-and-use-an-ignorerecommendationstxt-text-file)
   - [Verify that recommendations are ignored](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#to-verify-that-recommendations-are-ignored)
 - [SQL Health Check solution FAQ](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#sql-health-check-solution-faq)
 - [Additional Help](https://docs.microsoft.com/azure/azure-monitor/insights/sql-assessment#next-steps)
