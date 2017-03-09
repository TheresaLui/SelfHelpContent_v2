<properties
    pageTitle="What is the difference between deleting a VM in a Scale Set"
    description="What is the difference between deleting a VM in a Scale Set"
    service="scalesets"
    author="negat"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# What is the difference between deleting a VM in a Scale Set, vs. deallocating the VM? When should I choose one over the other?

The main difference is that deallocate doesn’t delete the VHDs, so there are storage costs associated with stop deallocate. Reasons you might use one over the other include:
- You want to stop paying Compute but keep the disk state of the VMs.
- You want to start a set of VMs faster than scaling out a scale set.
  - related to this scenario, you created your own autoscale engine and want faster end to end scale.
  - You have a scale set that is unevenly distributed across FD/UDs (due to selectively deleting VMs or due to VMs being deleted after overprovisioning). Stop deallocate followed by start on the scale set will evenly distribute the VMs across FD/UDs.
## Updates