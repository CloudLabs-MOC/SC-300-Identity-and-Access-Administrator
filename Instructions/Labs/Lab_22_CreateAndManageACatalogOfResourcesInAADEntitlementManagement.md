# Lab 22: Create and manage a catalog of resources in Azure AD entitlement management

## Lab scenario

A catalog is a container of resources and access packages. You create a catalog when you want to group related resources and access packages. Whoever creates the catalog becomes the first catalog owner. A catalog owner can add additional catalog owners. You must create and configure a catalog in your organization.

## Estimated time: 15 Minutes

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1 - Create a catalog
+ Task 2 - Create a groups
+ Task 3 - Add resources to a catalog
+ Task 4 - Add additional catalog owners
+ Task 5 - Edit a catalog
+ Task 6 - Create Access reviews for guest users
+ Task 7 - Delete a catalog


### Architecture Diagram

   ![](./media/arch22.png)

### Exercise 1 - Building out resources in Entitlement Management
Building out resources in Entitlement Management involves defining and structuring the catalog of resources and services available to users, streamlining access management within an organization.

### Task 1 - Create a catalog

1. In **Search, resources, services and docs**, search **Microsoft Entra ID (1)** and select for **Microsoft Entra ID (2)**.

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-1.png)

1. Under **Manage** section, select **Identity Governance**.

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-2.png)

1. From the left-hand navigation menu, under **Catalogs**, select **Catalogs (1)** and on the top menu, select **+ New Catalog (2)**.

    ![Screen image displaying the Identity governance catalog page with the New catalog menu highlighted ](./media/lab22-3.png)

1. In the New catalog pane, specify the following details and click on **Create (5)**.

      | **Option**                          | **Value**                               |
      | ----------------------------------- | --------------------------------------- |
      | **Name**                            | **Marketing (1)**                     |
      | **Description**                     | Enter **For marketing department users. (2)**|
      | **Enabled**                         | **Yes (3)** |
      |**Enabled for external users** | Select **No (4)**|
   

   ![Screen image displaying the Identity governance catalog page with the New catalog menu highlighted ](./media/lab22-4-(1).png)

1. You may choose to enable the catalog for immediate use or disable if you intend to stage it or keep it unavailable until you intend to use it. For this exercise, the catalog does not need to be enabled.

### Task 2 - Create a groups

1. In **Search, resources, services and docs**, search  **Microsoft Entra ID (1)** and select for **Microsoft Entra ID (2)**.

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-1.png)

1. From the left-hand navigation pane, select **Groups (1)**. On **Groups | All groups (2)**, select **New Group (3)**.

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-400.png)

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-401.png)

1. Now, follow these instruction to create a groups, then select **Create (4)**.

    | Settings | Value |
    | -------- | ------ |
    | Group type | **Security (1)** |
    | Group name | **Retail (2)** |
    | Group description | **Groups and Teams (3)** |

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-402.png)

1. On **Groups | All groups**, select **New Group**.

1. Now, follow these instruction to create a groups, then select **Create (4)**.

    | Settings | Value |
    | -------- | ------ |
    | Group type | **Security (1)** |
    | Group name | **Box (2)** |
    | Group description | **Applications (3)** |

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-403.png)

1. On **Groups | All groups**, select **New Group**.

1. Now, follow these instruction to create a groups, then select **Create (4)**.

    | Settings | Value |
    | -------- | ------ |
    | Group type | **Security (1)** |
    | Group name | **Salesforce (2)** |
    | Group description | **Applications (3)** |

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-404.png)

1. On **Groups | All groups**, select **New Group**.

1. Now, follow these instruction to create a groups, then select **Create (4)**.

    | Settings | Value |
    | -------- | ------ |
    | Group type | **Security (1)** |
    | Group name | **SharePoint sites (2)** |
    | Group description | **SharePoint (3)** |

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-405.png)

    > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
    > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task.
    > - If not, carefully read the error message and retry the step, following the instructions in the lab guide. 
    > - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.

     <validation step="37c693fb-cab4-469c-855b-5e0afd7108df" />

### Task 3 - Add resources to a catalog

To include resources in an access package, the resources must exist in a catalog. The types of resources you can add are groups, applications, and SharePoint Online sites. The groups can be cloud-created Microsoft 365 Groups or cloud-created Entrta ID security groups. The applications can be Entra ID enterprise applications, including both SaaS applications and your own applications federated to Entra ID. The sites can be SharePoint Online sites or SharePoint Online site collections.

1. In **Search, resources, services and docs**, search and select for **Microsoft Entra ID**.

1. Under **Manage** section, select **Identity Governance**.

1. On the Identity Governance page, under **Entitlement management**.

1. In the **Catalogs (1)** list, select **Marketing (2)**.

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-406.png)

1. From the left-hand navigation pane, under **Manage**, select **Resources (1)** and on the menu, select + **Add resources (2)**.

   ![](./media/lab22-5.png)

1. Select **+ Groups and Teams (1)**. In the Add resources to catalog page, review the available options. Add the following items: **Box**, **Retail**, **Salesforce**, and **SharePoint sites (2)**, then click on **Select (3)**.

   ![](./media/lab22-6.png)

1. Back on **Add recources to catalog** page and click on **Add**, these resources can now be included in access packages within the catalog.

     ![](./media/lab22-7.png)
     >**Note**: For this exercise, it is okay to choose any resource you may have available.

### Task 4 - Add additional catalog owners

The user that created a catalog becomes the first catalog owner. To delegate management of a catalog, you add users to the catalog owner role. This helps share the catalog management responsibilities.

1. If necessary, in the Azure portal, browse to **Microsoft Entra ID**, from the left-hand navigation pane, select **Identity Governance** and select **Catalogs** and then select **Marketing**.

2. In the Marketing catalog page, from the left-hand navigation pane, select **Roles and administrators (1)**, select **+ Add catalog owner (2)** and Select members pane opens, select your **Adele Vance** and then select **Select**.
   
   ![](./media/lab22-9.png)

5. Review the newly added role in the Roles and administrators list.

### Task 5 - Edit a catalog

You can edit the name and description for a catalog. Users see this information in an access package's details.

1. On the Marketing page, from the left-hand navigation pane, select **Overview (1)**, then on the top menu, select **Edit (2)**.

    ![Screen image displaying the Azure resources discovery page with the subscription and manage resource highlighted](./media/lab22-407.png)

1. On the **Overview (1)** page review the setting and, under **Properties** > **Enabled**, select **Yes (2)** and click  **Save (3)**.

    ![](./media/lab22-10.png)

### Task 6 - Create Access reviews for guest users

1. Navigate back to the **Identity Governance**.

1. Access reviews can manage the access lifecycle. Entra ID Identity Governance provides an overview dashboard showing the status of access reviews.

1. From the left-hand navigation pane, select **Access reviews** under **Access reviews (1)** and select **+ New access review (2)** to create your guest user access review.  The tile will open to configure the access review for guest users.

    ![](./media/lab22-11.png)

1. On tile under the **Review access to a resource type**, choose **Select**

    ![](./media/lab22-408.png)

1. On **New access review** blade, specify the following detail and click on **Next: Reviews (4)**.
    | Settings | Value |
    | -------- | ------ |
    | **Select what to review** | **Teams + Groups (1)** |
    | **Review scope** | select **All Microsoft 365 groups with guest users (2)** |
    | **Scope** | **Guest users only (3)** |
    |||

   ![](./media/lab22-12.png)

1. The next tile is where you configure who reviews and approves access, how often access will be reviewed, and when access will expire.

1. Under **Select reviewers**, select **Group owners (1)** as these reviewers, enter a **Duration (in days) (2)**, default is 3, choose a **Review recurrence (3)** and **Start date (4)** for the review click on **Settings (5)**.

    ![](./media/lab22-20.png)

    >**Note**: Guest users should not be allowed to review their own access as a good identity governance practice.
    
1. Select **Next: Settings** and configure the settings for how the review will take place and what happens when the guest user responds or does not respond.  A good practice is to select **Auto apply results to resource (1)** and select **Remove access (2)** for **If reviewers don't respond** and click on **Next: Review + Create (3)**,
    
    ![](./media/lab22-21.png)

1. Select **Create** to create the new **Access review**.

    ![](./media/lab22-22.png)

### Review

In this lab, you have completed:

- Created a catalog
- Create a groups
- Added resources to a catalog
- Added additional catalog owners
- Edited a catalog
- Created Access reviews for guest users

### You have successfully completed the lab
