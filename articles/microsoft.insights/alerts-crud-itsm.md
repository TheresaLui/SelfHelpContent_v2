<properties
    pageTitle="Configuring the ITSM action"
    description="I'm trying to create, edit or delete an ITSM integration action but I don't know how to configure it"
    infoBubbleText=""
    service="microsoft.insights"
    resource="actiongroups"
    authors="nolavime"
    ms.author="nolavime"
    displayOrder="1"
    articleId="alerts-crud-itsm"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32739776"
    resourceTags=""
    productPesIds="15454"
    ccloudEnvironments="public,fairfax,mooncake,usnat,ussec"
    ownershipId="AzureMonitoring_ActionGroup"
/>

# **I'm trying to create, edit or delete an ITSM integration action but I don't know how to configure it**

## ITSM

The IT Service Management Connector (ITSMC) allows you to connect Azure and a supported IT Service Management (ITSM) product/service.
I'm trying to create, edit or delete an ITSM integration action but I don't know how to configure it

## Recommended Steps

If you are facing issues while trying to setup ITSM the following steps to troubleshoot:

1. Check that [ITSM Connector](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-overview#adding-the-it-service-management-connector-solution) is installed
2. In case you are using **Service Now**:
    * Check that [connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-1) in the ITSM solution workspace and check if all the details are correct: URL, Username/Password, Client ID/Client Secret.
    * Check that you defined correctly the [Oauth connection](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-1) in ServiceNow instance.
    * Check that the [User App](https://store.servicenow.com/sn_appstore_store.do#!/store/application/ab0265b2dbd53200d36cdc50cf961980/1.0.1) for Microsoft Log Analytics integration is installed.
    * Check that [integration user](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#create-integration-user-role-in-servicenow-app) role for the user app is configured correctly.
3. In case you are using **System Center Service Manager**
    * Check that [connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure) in the ITSM solution workspace and check if all the details are correct.
    * Check that The Service Manager [Web application](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#create-and-deploy-service-manager-web-app-service) (Web app) is deployed and configured.
    * Check that [Hybrid connection](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#configure-the-hybrid-connection) created and configured.
4. In case you are using **Provance**
    * Check that [connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-2) in the ITSM solution workspace and check if all the details are correct.
    * Provance [App should be registered with Azure AD](https://docs.microsoft.com/azure/app-service/configure-authentication-provider-aad) - and client ID is made available.
5. In case you are using **Cherwell**
    * Check that [connection details](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#connection-procedure-3) in the ITSM solution workspace and check if all the details are correct.
    * Check that the [Client ID generated](https://docs.microsoft.com/azure/azure-monitor/platform/itsmc-connections#generate-client-id-for-cherwell).
