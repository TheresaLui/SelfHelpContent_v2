<properties
    pageTitle="Avere vFXT Upgrade Assistance"
    description="Provide assistance with Avere vFXT upgrades."
    infoBubbleText="Avere vFXT Upgrade Assistance"
    authors="jbut"
    ms.author="jebutl"
    displayOrder="1"
    articleId="averevfxt-upgradeassist"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32609697"
    resourceTags=""
    productPesIds="16506"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>

# Avere vFXT Upgrade Assistance

The following article provides simple steps for upgrading an Avere vFXT cluster.

## **Recommended Steps**

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

## **Recommended Documents**

* [Software Update Instructions](https://azure.github.io/Avere/legacy/ops_guide/4_7/html/gui_software_update.html)

