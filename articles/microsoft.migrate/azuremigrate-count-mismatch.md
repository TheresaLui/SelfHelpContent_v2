<properties
    pageTitle="Count of discovered, assessed or migrated machines is incorrect" 
    description="Issues and guidance regarding creating a new migrate project and adding a tool" 
    service="microsoft.migrate"
    resource="migrateprojects"
    authors="ponatara"
    ms.author="ponatara"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32675737, 32675738, 32675739"
    resourceTags=""
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec" 
    articleId="72de9298-2a3f-4d0d-96c5-b2b5886483e6"
 	ownershipId="Compute_AzureMigrate"
/>

# Count of discovered, assessed or migrated machines is incorrect
  
## **Recommended Steps**
  
### **I am not able to see the right number of discovered, assessed or migrated machines in the Azure Migrate: Server Assessment or Azure Migrate: Server Migration tile(s) on the 'Servers' page**

1. This is likely a temporary issue. If you have triggered discovery for a VMware environment, wait for up to 15 mins and then refresh the details of the project by clicking on 'Refresh' on the 'Servers' page. If you have triggered discovery for your Hyper-V environment, wait for up to 30 mins and then refresh the details of the project by clicking on 'Refresh' on the 'Servers' page. If you still don't see the right number of machines reflecting on the 'Servers' page, follow the guidance listed in the next step.

2. This issue can occur if you have discovered the same set of machines using two or more on-premises appliances registered to the same project. Make sure that you specify a different scope of machines for discovery from each appliance i.e. the same machine has not been discovered by two or more appliances. After you have reset the scope of discovery for each of the appliances, go to the 'Overview' page of Azure Migrate: Server Assessment, click on 'Agent health' and then click on 'Refresh agent'. This will trigger synchronization of discovery data from the on-premises appliance. Follow the steps listed [here](https://aka.ms/migrate/self-help/count-mismatch-issues) for more details.

### **I am not able to see the right number of discovered, assessed or migrated machines in a non-Microsoft ISV tool**

Occasionally, there may be a data sync issue between the non-Microsoft ISV tool and Azure Migrate. This should correct itself within 24-hours. If the issue persists, please contact the ISV's support team.
