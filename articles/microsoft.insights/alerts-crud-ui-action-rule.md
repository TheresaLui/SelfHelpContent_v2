<properties
    pageTitle="Issue while creating, updating, or deleting an action rule"
    description="I am trying to create, edit or delete an action rule but I'm getting an error, or I don't know how to configure it"
    infoBubbleText=""
    service="microsoft.alertsmanagement"
    resource="actionRules"
    authors="ofirmanor, neilghuman"
    ms.author="ofmanor,neghuman"
    displayOrder="8"
    articleId="alerts-crud-ui-action-rule"
    selfHelpType="generic"
    supportTopicIds="32739777"
    productPesIds="15454"
    cloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# **Issue while creating, updating or deleting an action rule**
If you are trying to create, update, or delete an [action rule](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-action-rules) in the portal, but receiving unexpected errors, follow these steps:

## **Recommended Steps**
[![Monitoring Video](https://docs.microsoft.com/en-us/azure/azure-monitor/app/media/troubleshoot/alerts/how-to-create-action-rules-1920.png)](https://www.microsoft.com/videoplayer/embed/RE4rBZ2)

### Are you receiving a permission error?

Ensure you have the permissions to author the action rule. Usually, you would use the ["Monitoring Contributor"](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#monitoring-contributor) built-in role.

### Have you configured all the action rules parameters correctly?

Follow the action rule documentation of explanation of each parameter.
