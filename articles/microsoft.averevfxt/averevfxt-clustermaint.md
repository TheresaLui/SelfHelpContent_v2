<properties
    pageTitle="Avere vFXT Cluster Maintenance Activity"
    description="Resolve issues with Avere vFXT cluster maintenance."
    infoBubbleText="Avere vFXT Cluster Maintenance Activity"
    authors="jbut"
    ms.author="jebutl"
    displayOrder="1"
    articleId="averevfxt-clustermaint"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32609688"
    resourceTags=""
    productPesIds="16506"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>

# Avere vFXT Cluster Maintenance Activities

The following advice may help you perform cluster maintenance activities.

### Key Considerations for Cluster Maintenance

Here are some key things to consider before performing cluster maintenance. First, does the activity require pre-planning? In most cases, these activities will need to be planned. Regardless how minor the activity is, there is typically some impact on the ability for clients to access data.

You should determine the estimated timeframe for the activity. This timeframe will drive any timeframes that you communicate to your user community regarding storage outages. The timeframe should include the start time as well as the duration of the maintenance activity.

Common cluster maintenance activities include: software upgrades, restarting services, and rebooting nodes.

### *Software Upgrades*

You may download the software via a URL provided by Microsoft Support, or you may visit our support [portal](https://averesystems.force.com/support/) to select and download a software package.

Please follow the following steps to upgrade your cluster:

1. Log into your Avere Control Panel and click the Settings tab at the top of the page
2. On the left side of the page, under the Administration heading, click the Software Update link
3. Enter the download URL from above into the Download URL field, or choose to download the file locally and upload it using the Choose File button at the bottom of the page
4. Depending on your choice in Step 3, click either the Download to alternate image location or Upload to alternate image location button
5. Check the box for Activate in High Availability Mode
6. Once the nodes download and install the package, click the Activate alternate image button

The nodes will then proceed to restart and boot into the new Avere OS version one by one.  You may notice some slight interruption in performance while the upgrade is being performed as the client facing IP addresses are rebalanced.

Also, after performing an upgrade, it is an Avere best practice to reset your cluster password.  You may keep the password the same as what you currently have set.  The purpose of the password reset is to force the system to rewrite the password hashes to utilize the Password-Based Key Derivation Function 2 (PBKDF2).

You can reset your password in the Avere Control Panel by following these instructions:

1. Log into your Avere Control Panel and click the Settings tab at the top of the page
2. On the left side of the page, under the Administration heading, click Users
3. In the table of users, next to "admin," click Password
4. Enter your new password into the fields at the top of the page
5. Click Submit

### *Restarting Services*

Sometimes it is helpful to restart services in order to resolve issues. You may restart services via the following steps:

1. Navigate to the Administration -> System Maintenance section of the Avere Control Panel
2. Determine whether you want to perform a high-availability (HA) restart or a non-HA restart. An HA restart minimizes the disruption to clients, but it may extend the overall amount of time that the operation will run. A non-HA restart is useful if you're not concerned about the impact on clients. HA restarts will restart services on one node at a time.
3. Click the "Restart cluster" button

### *Rebooting Nodes*

Rebooting nodes is a way to completely restart our system.  Rebooting is a more powerful restart than just restarting services.  Reboots sometimes provide a way to remediate issues, but more often than not, a service restart is sufficient.  Service restarts should almost always be tried prior to reboots.

In order to reboot, do the following:

1. Navigate to the Administration -> System Maintenance section of the Avere Control Panel
2. Determine whether you want to perform a high-availability (HA) restart or a non-HA reboot. An HA reboot minimizes the disruption to clients, but it may extend the overall amount of time that the operation will run. A non-HA reboot is useful if you're not concerned about the impact on clients. HA reboots will reboot one node at a time.
3. Click the "Reboot cluster" button

## **Recommended Documents**

* [Software Update Instructions](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/gui_software_update.html)
* [Restart Services and Reboot Instructions](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/gui_system_maintenance.html)

