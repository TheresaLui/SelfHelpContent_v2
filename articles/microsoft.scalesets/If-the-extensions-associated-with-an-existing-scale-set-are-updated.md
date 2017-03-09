<properties
    pageTitle="If the extensions associated with an existing scale set are updated"
    description="If the extensions associated with an existing scale set are updated"
    service="scalesets"
    author="negat"
    displayOrder="48"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# If the extensions associated with an existing scale set are updated, would they affect already existing VMs? (that is, would the VMs show up as not matching the scale set model)? Or would they be ignored? When an existing machine is service-healed / reimaged / etc. would the scripts that are currently configured on the scale set be executed or would the ones that were configured when the machine was first created be used?

- If the extension definition in the scale set model is updated, it would update the VMs if upgradePolicy was set to automatic, and they would be flagged as not matching the model if upgradePolicy is set to manual. 
- If an existing VM is service healed, it would appear like a reboot and the extensions would not rerun. If it is reimaged it would be like replacing the OS drive with the source image and any specialization from the latest model, such as extensions would run.