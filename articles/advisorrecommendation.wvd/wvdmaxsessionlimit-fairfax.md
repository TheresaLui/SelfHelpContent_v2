<properties 
    pageTitle="Change the max session limit for your depth first load balanced host pool to improve VM performance" 
    description="Change the max session limit for your depth first load balanced host pool to improve VM performance" 
    authors="sefriend" 
    ms.author="rdinfra" 
    articleId="_Fairfax" 
    selfHelpType="advisorRecommendationMetadata" 
    cloudEnvironments="Fairfax" 
    ownershipId="Windows_Virtual_Desktop" 
/> 
# Change the max session limit 
--- 
{ 
  "recommendationOfferingId": "1132b618-fefe-40a0-9256-e685ff575ac7", 
  "recommendationOfferingName": "Windows Virtual Desktop", 
  "$schema": "AdvisorRecommendation", 
  "recommendationTypeId": "", 
  "dataSourceMetadata": { 
    "streamNamespace": "cluster('https://rdsprodus2.westus2.kusto.windows.net').database('WVD').ChangeMaxSessionLimitForDepthFirstHostPool", 
    "dataSource": "Kusto", 
    "refreshInterval": "0.00:01:00" 
  }, 
  "recommendationCategory": "Performance", 
  "recommendationImpact": "High", 
  "recommendationResourceType": "Microsoft.DesktopVirtualization/hostpools", 
  "recommendationFriendlyName": "ChangeMaxSessionLimitForDepthFirstHostPool", 
  "recommendationMetadataState": "Active", 
  "owner": { 
    "email": "rdinfra@microsoft.com", 
    "icm": { 
      "routingId": "mdm://adspartner/VirtualDesktop", 
      "service": "Windows Virtual Desktop", 
      "team": "Windows Virtual Desktop" 
    }, 
    "serviceTreeId": "362c0db7-c08b-4471-93ef-c90effc930dd" 
  }, 
  "ingestionClientIdentities": [], 
  "version": 1.0, 
  "learnMoreLink": "https://docs.microsoft.com/en-us/azure/virtual-desktop/configure-host-pool-load-balancing", 
  "description": "Change the max session limit for your depth first load balanced host pool to improve VM performance ", 
  "longDescription": "Depth first load balancing uses the max session limit to determine the maximum number of users that can have concurrent sessions on a single session host. If the max session limit is too high, all user sessions will be directed to the same session host and this may cause performance and reliability issues. Therefore, when setting a host pool to have depth first load balancing, you should also set an appropriate max session limit according to the configuration of your deployment and capacity of your VMs. To fix this, open your host pool's properties and change the value next to the \"Max session limit\" setting.", 
  "potentialBenefits": "Ensure session host functional stability, reliability, and performance when using Windows Virtual Desktop service", 
  "actions": [ 
    { 
      "actionId": "", 
      "description": "Change the max session limit for your depth first load balanced host pool", 
      "actionType": "Blade", 
      "extensionName": "Microsoft_Azure_WVD", 
      "bladeName": "HostpoolOverviewBlade", 
      "metadata": { 
        "id": "{resourceId}" 
      } 
    } 
  ], 
  "resourceMetadata": { 
    "action": { 
      "actionId": "", 
      "actionType": "Blade", 
      "extensionName": "Microsoft_Azure_WVD", 
      "bladeName": "HostpoolOverviewBlade", 
      "metadata": { 
        "id": "{resourceId}" 
      } 
    } 
  }, 
  "displayLabel": "Change the max session limit for depth first load balanced host pools", 
  "additionalColumns": [], 
  "tip": "Change the max session limit for your depth first load balanced host pool to improve VM performance." 
} 
--- 