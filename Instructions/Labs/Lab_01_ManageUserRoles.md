 
# Lab 01: Manage User Roles

## Lab scenario

Your company recently hired a new employee who will perform duties as an application administrator. You must create a new user and assign the appropriate role.

#### Estimated time: 60 minutes

## Lab Objectives

After completing this lab, you will be able to complete the following exercises:

-  Exercise 1 - Create a new user and test their application admin rights
-  Exercise 2 - Assign the application admin role and create an app
-  Exercise 3 - Remove a role assignment
-  Exercise 4 - Bulk import of users
-  Exercise 5 - Remove a user from Microsoft Entra ID
-  Exercise 6 - Add a  license to a user account

## Architecture Diagram

![Bulk import using csv file entry](./media/archentra.png)

## Exercise 1 - Create a new user and test their application admin rights
  
  In this exercise, you will create  a new user account and verify their administrative privileges by testing their application access and control.

### Task 1 - Add a new user

1. In the Azure portal, search for **Microsoft Entra ID (1)** and  select **Microsoft Entra ID (2)** from the services.

    ![](./media/sc300--1.png)

1. In the left navigation menu, under **Manage**, select **Users**.

    ![](./media/sc300-2.png)

1. Then select **+ New User (1)** and **Create new user (2)**.

    ![](./media/sc300-3.png)

1. Then, create a user with the following information:

    | **Setting**| **Value**|
    | :--- | :--- |
    | User principal name| ChrisG **(1)**|
    | Display Name| Chris Green **(2)**|
    
    - Mark the **Auto-generate password (3)** option.

    - Copy the generated **password** **(4)** to a location you can remember it for the next task.

    - Copy the **userprincipalname (5)** Of Chris Green in order to login in the next task

    - Click on **Review+create (6)**

      ![](./media/sc300-4.png)    

       >**Note:** You will have to change the password upon first login to this account
      
1. Thne click on **Create**.

1. The user is now created and registered to your organization.

    ![](./media/sc300-5.png)

### Task 2 - Login and try to create an app

1. Launch a new **InPrivate** browser window.

1. Open the Azure Portal [https://portal.azure.com](https://portal.azure.com) as Chris Green.

1. Enter the Chris Green's **Userprincipalname** that you had copied in task 1 **(1)** then click on **Next (2)**.

    | **Setting**| **Value**|
    | :--- | :--- |
    | User name| ChrisG@`your domain name.com`|

    ![](./media/sc300-6.png)

1. Enter the auto-generated password from previous task **(1)** then click on **Next (2)**.

    ![](./media/sc300-7.png)

1. Update your password and click on **Sign in (4)**.

    | **Setting**| **Value**|
    | :--- | :--- |
    | Current Password| Use auto-generated password **(1)**|
    | New Password| Enter **Horizon@123 (2)** |
    | Confirm Password| Reenter **Horizon@123 (3)** |

    ![](./media/sc300-8.png)    

1. Click on **Next** for **Action Required** pop up.

    ![](./media/sc300-9.png)

     >**Note:** If you don’t have the Microsoft Authenticator app installed on your mobile device:

      - Open **Google Play Store** (Android) or **App Store** (iOS).
      - Search for **Microsoft Authenticator** and tap **Install**.
      - Open the **Microsoft Authenticator** app, select **Add account**, then choose **Work or school account**.
      - A **QR code** will be displayed on your computer screen.
      - In the Authenticator app, select **Scan a QR code** and scan the code displayed on your screen.
      - After scanning, click **Next** to proceed.
      - On your phone, enter the number shown on your computer screen in the Authenticator app and select **Next**.

1. If prompted to stay signed in, you can click **No**.
 
1. If you see a **Welcome to Microsoft Azure** window dialog, Select the **Cancel** button.

1. Search for and select **Enterprise applications (1)** in the search dialog at the top of the screen and select **Enterprise applications (2)** from the services.

    ![](./media/sc300-10.png)

1. Select on **+ New application**.

    ![](./media/sc300-11.png)

1. Notice that **+ Create your own application** is **unavailable**.

    ![](./media/sc300-12.png)

1. Try Selecting on some of the other settings like **User settings**, and others to see the **Chris Green** does not have rights.

    ![](./media/sc300-13.png)

1. Select on **ChrisG** name in the upper-right corner and sign out.

    ![](./media/sc300-14.png)

## Exercise 2 - Assign the application admin role and create an app

 Using Microsoft Entra ID, you can designate limited administrators to manage identity tasks in less-privileged roles. Administrators can be assigned for such purposes as adding or changing users, assigning administrative roles, resetting user passwords, managing user licenses, and managing domain names.

### Task 1 - Assign a role to a user

1. Go back to the normal browser window where you are logged in as a Global Administrator.

1. Navigate to **Microsoft Entra ID**  page.

1. Select on **Users** under the Manage section of the menu.

1. Select **Chris Green's** account.

1. Choose **Assigned roles** from the Manage menu.**(1)**

    - Select **+ Add assignments (2)**
    - Search for **Application administrator (3)**
    - Then mark the `Application administrator` role **(4)**
    - Select **Add (4)**

      ![Assigned roles page - showing the selected role](./media/sc300-15.png)

1. Select the **Refesh** button.

1. The newly assigned Application administrator role appears on the user’s Assigned roles page.

    ![](./media/sc300-16.png)

     > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
     > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
     > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
     > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help

     <validation step="a2dbf6f4-a68f-47d8-b0fe-f5e0e821e10f" />

### Task 2 - Check application permissions

1. Launch a new InPrivate browser window.

1. Open the Azure Portal [https://portal.azure.com](https://portal.azure.com) as Chris Green.

    | **Setting**| **Value**|
    | :--- | :--- |
    | User name| ChrisG@`your domain name.com` (Enter the **Userprincipalname**)|
    | Password| Enter the unique and secure password you created earlier **Horizon@123** |

    - If prompted, click on **Next** for **Action Required** pop up.

      >**Note:** If you don’t have the Microsoft Authenticator app installed on your mobile device:

      - Open **Google Play Store** (Android) or **App Store** (iOS).
      - Search for **Microsoft Authenticator** and tap **Install**.
      - Open the **Microsoft Authenticator** app, select **Add account**, then choose **Work or school account**.
      - A **QR code** will be displayed on your computer screen.
      - In the Authenticator app, select **Scan a QR code** and scan the code displayed on your screen.
      - After scanning, click **Next** to proceed.
      - On your phone, enter the number shown on your computer screen in the Authenticator app and select **Next**.
      - If prompted to stay signed in, you can click **No**.
      - If you see a **Welcome to Microsoft Azure** window dialog, Select the **Cancel** button.

1. Search on and select **Enterprise applications (1)** in the search dialog at the top of the screen and select **Enterprise applications (2)** from the services.

    ![](./media/sc300-10.png)

1. Click on  **+ New Application**.

1. Notice that **+ Create your own application** is **available** now.

    ![](./media/sc300-17.png)

     >**Note:** This role now has the ability to add applications to the tenant.  We will experiment more with this feature in later labs.

1. Sign out of the Chris Green instance of the Azure Portal and close the browser.

    ![](./media/sc300-14.png)

## Exercise 3 - Remove a role assignment

In this exercise, you will remove the role assignment that was assigned in the previous task.

### Task 1 - Remove the application administrator from Chris Green

This task will use an alternative method to remove the assigned role; it will use the **Roles and administrators** option in Entra ID.

1. If you are not already logged in as your Global Admin, launch the Azure Portal and log in now.

1. In the search box type **Microsoft Entra ID** and launch Microsoft Entra ID.

1. Select on **Users** under the Manage section of the menu.

1. Select **Chris Green's** account.

1. From the left navigation pane, click on **Assigned Roles (1)**.

    - Put a check in the box next to **Application Administrator (2)**.

    - Select **X Remove assignments (3)** from the options at the top navigation pane.

      ![](./media/sc300-18.png)    

1. Answer **Yes** when the confirmation box opens.

1. Close Microsoft Entra ID.

## Exercise 4 - Bulk import of users

### Task 1 - Bulk operations for creating users with a .csv file

1. In your Lab Vm  navigate to **C:\AllFiles\AllFiles.zip\SC-300-Identity-and-Access-Administrator-prod\Allfiles\Labs\Lab1 (1)** press **Enter** and open the **SC-300BulkUser (2)** excel file and modify the domain names for all the users.

    ![](./media/sc300-19.png)

1. Select **Sign in or create account**.

    ![](./media/sc300-20.png)

     >**Note:** Sign in with the ODL user credentials present in the **Environment page** in order to be able to edit the excel sheet.
      
1. The .csv template provides you with the fields included with the user profile. This includes the required username, display name, and initial password.The following screenshot is an example of how you can complete the .csvfile: 

    ![Bulk import using csv file entry](./media/bulk121.png)
       
3. Copy the domain name  in the Azure portal from the Microsoft Entra ID Overview page, copy the primary domain name, and replace **<<<enter your >>>** with primary domain name for all the users.

   ![Bulk import using csv file entry](./media/xce12.png)

   >**Note:** You do not need to fill out all the fields. As per the sample data provided, you mainly need to add the username information. Be careful not to leave any extra white spaces in the Excel sheet else Bulk creation will fail.

1. Once you are done with replacing the domain names, navigate to **Downloads (1)** section, save the file as **BulkUser (2)** then click on **Save ()3** and then close the file.

    ![](./media/sc300-21.png)

1. In the Microsoft Entra ID menu, select **Users** under **Manage**.

1. On the **Users | All users** tile, select the **Bulk operations (1)** drop-down arrow and then **Bulk create (2)**.

    ![](./media/sc300-22.png)

1. Selecting **Bulk create** will open a new tile. From the **upload** button **(1)** browse to **Downloads (2)** section and choose the file named as **BulkUser (3)** and select **Open (4)**.

    ![](./media/sc300-23.png)

1. You will be notified that the file has been uploaded successfully. Choose **Submit** to add the users. 

    ![](./media/sc300-24.png)

1. After the users have been created, you will be prompted that the creation has succeeded.  Close the Bulk create users tile and the new users will be populated in the list of **Users | All users**.

   ![Bulk import using csv file entry](./media/newcruser.png)

   >**Note:** Refresh the page to see the users

### Task 2 - Addition of users using PowerShell

1. In the LabVM, search for **powershell (1)**, right click on **Windows Powershell (2)** and then open PowerShell as an administrator **(3)**. 

    ![](./media/sc300-25.png)

     >**Note** - Select **PowerShell** and not **PowerShell ISE**.

1. You will need to add and import the Azure AD PowerShell module if you have not used it before.  Run the following two commands and when prompted to confirm press Y:

    ```
    Install-Module AzureAD
    Import-Module AzureAD
    ```

1. Confirm that the module is installed correctly by running the command:  

    ```
    Get-Module AzureAD 
    ```

    ![](./media/sc300-26.png)    

1. Next, you will need to login to Azure by running:  

    ```
    Connect-AzureAD 
    ``` 

    ![](./media/sc300-27.png) 

1. The Microsoft login window will appear for you to log in to Azure AD.  

   >**Note:** If you get any warnings you can click on **Yes**

1. To verify that you are connected and to see existing users, run:  

    ``` 
    Get-AzureADUser 
    ```

    ![](./media/sc300-28.png)     
    
1. To assign a common temporary password to all new users, run the following command. 
    ``` 
    $PasswordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
    ```

    ```
    $PasswordProfile.Password = "Horizon@123" 
    ```

1. You are ready to create a new users.  The following command will be populated with the user information and run.  If you have more than one user to add, you can use a notepad txt file to add the user information and copy/paste into PowerShell. 

    ```
    New-AzureADUser -DisplayName "New User" -PasswordProfile $PasswordProfile -UserPrincipalName "NewUser@labtenantname.com" -AccountEnabled $true -MailNickName "Newuser"
    ```

    ![](./media/sc300-29.png)     

     >**Note** - Replace **labtenantname.com** with the domain name  you  copied in **Exercise 4 Task 1 step number 3**. 

## Exercise 5 - Remove a user from Microsoft Entra ID

It may happen that an account is deleted and then needs to be recovered. You need to verify you can recover an account that has been deleted recently.

### Task 1 - Remove a User

1. Back in the Azure portal,in the search box type **Microsoft Entra ID** and launch Microsoft Entra ID.

1. In the left navigation, under **Manage**, select **Users**.

1. In the **Users** list, select the check box for a user that will be deleted. For example, select **Chris Green (1)**. With the user account selected, on the menu, select **Delete (2)**.

    **Tip** - Selecting users from the list allows you to manage multiple users at the same time. If you select the user, to open that user’s page, you will only be managing that individual user.

    ![Screen image displaying the All users users list with one user check box selected and another check box highlighted indicating the ability to select multiple users from the list.](./media/sc300-30.png)

1. Review the dialog box and then select **Ok**.

## Task 2 - Restore a deleted user

1. In the Users page, in the left navigation, select **Deleted users (1)**. Review the list of deleted users and select **Chris Green (2)**. On the menu, select **Restore user (3)**.

    ![](./media/sc300-31.png)

     >**Important** - By default, deleted user accounts are permanently removed from Azure Active Directory automatically after 30 days
     .
1. Review the dialog box and then select **OK**.

1. In the left navigation, select **All users (1)**. Search for select **Chris Green (2)** and the verfy that the user has been restored **(3)**.

    ![](./media/sc300-32.png)

   >**Note:** You might have to click on **Refresh** to veiw the restored user.

## Exercise 6 - Add a  license to a user account

Some user accounts in your organization will not be provided all available products in their assigned license or will need updates or additions to their license assignment. You need to ensure you are able to update a user account's license assignment in Microsoft Entra ID.

### Task 1 - Find your unlicensed user in Microsoft Entra ID

1. In the Azure portal, navigate to Microsoft Entra ID, from the left navigation pane under **Manage**, select **Users**.

1. In the Users page, enter **Andre** into the search box. Select on **Andre Lawson (2)**.

    ![](./media/sc300-33.png)

1. Review Andre's profile and ensure he has a Usage Location set.

    >**Warning** - To assign a license to a user, the user must assigned a usage location.

1. To check if Andre has a usage location set, navigate to Andre Lawson's profile and choose **Edit Properties** from the top menu.

    ![](./media/sc300--34.png)

1. Navigate to the **Settings (1)** section and enter the location as **United States (2)** and click on **Save (3)**.

   ![Screen image displaying the Update license assignments page and license options highlighted](./media/sc300-35.png)

1. Now, back on the Overview page of Microsoft Entra ID, select the **Licenses (1)** menu item in the left-hand menu. Ensure that Andre has **No license assignments found (2)**. Select **Go to M365 Admin Center (3)** and you will be navigated to Microsoft 365 Admin Center.

    ![](./media/sc300-36.png)

1. From left pane select **Licenses (1)**  and select the available **Office 365 E5 license (2)**.

    ![](./media/sc300-37.png)

1. Select **+ Assign Licenses**.

    ![](./media/sc300-38.png)

1. On **Assign licenses to users** page, enter the name or email address of the user **(1)** to whom you want to assign the license and click on **Assign (2)**.

    ![](./media/sc300-39.png)

1. Now navigate to the user profile of **Andre Lawson**  from the left navigation pane select **Licenses (1)**. Notice that the license has been assigned **(2)**.

    ![](./media/sc300-40.png)

    >**Note:** You might have to refresh to see the License entry.

     > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
     > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
     > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
     > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help

     <validation step="d02480d1-77db-498c-8f14-61b3dbc8169b" />

## Review

In this lab, you have performed  the following tasks:

- Created a new user and test their application admin rights
- Assigned the application admin role and create an app
- Removed a role assignment
- Bulk imported users
- Removed a user from Microsoft Entra ID
- Added license to a user account

## You have successfully completed the lab
