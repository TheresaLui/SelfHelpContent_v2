<properties 
    pageTitle="Agent health and notification"
    description="Guidance regarding agent health and notification"
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="vikram1988"
    ms.author="vibansa"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675735"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="75vc4298-2a3f-4d0d-96c5-b2b5886483e6"
	ownershipId="Compute_AzureMigrate"
/>

# Guidance regarding agent health and notification

## **Recommended Steps**

### **How can I update my Azure Migrate appliance?**

By default, the appliance and the different installed agents on the appliance get updated automatically. The appliance checks for updates once every 24-hours. If there are any failures during the update process, retry behaviors kick in to handle the update.

Auto-update only updates the appliance and installed agents on the appliances. The OS is not updated. Use Microsoft Updates to ensure that the OS is always updated.

### **Can I turn off auto-update on the Azure Migrate appliance?**

Auto-update on the appliance can be turned off using the instructions provided [here](https://aka.ms/migrate/selfhelp/appliance/agenthealth). If you turn-off auto-update, you will have to manually update the appliance agents from the appliance management app.

Note that we strongly recommend that you keep auto-update enabled.

### **Can I check the health of the agents on the appliance?**

On Azure portal, navigate to the "Agent health" page in the Server Assessment or Server Migration tool. You can check the connection status of the discovery and assessment agents on the appliance to Azure.
