# Lab 28 - Monitor and manage security posture with Identity Secure Score

## Lab scenario

Microsoft Entra Identity Protection provides automated detection and remediation to identity-based risks, and provides data in the portal to investigate potential risks. Microsoft Entra Identity Protection also provides an Identity Secure Score to monitor and improve your identity security posture.  In the same manner as Microsoft Defender XDR and Microsoft Defender for Cloud, Identity Secure Score provides improvement actions and recommendations that can improve your overall security posture for identity in Microsoft Entra ID.  This lab will explore this capability. 

>**Note:** Since this lab is running on a new created tenant environment, you will probably get an Identity Secure Score of 30% or less.  It takes about 24 hours for viable data to enter the calculation to give you a valid score.


## Estimated time: 15 minutes

## Lab objectives

In this lab, you will complete the following tasks:

+ Task 1 - Review Identity Secure Score and improvement actions
+ Task 2 - Execute an improvement action

## Architecture Diagram

![Screen image displaying the New Group page with Group type, Group name, Owners, and Members highlighted](./media/arch28.png)


## Exercise 1 - Using Identity Secure Score to monitor and manage identity security posture

### Task 1 - Review Identity Secure Score and improvement actions

In this task, you will review the Identity Secure Score in Microsoft Entra and explore the improvement actions that enhance your organization's identity security posture. You'll navigate the dashboard to assess focused actions for boosting your overall tenant security.

1. Open a new tab, and sign in to the [https://entra.microsoft.com/](https://entra.microsoft.com/).

1. Sign in using below credentials :

   | Setting | Value |
   | :--- | :--- |
   | Username | **<inject key="AzureAdUserEmail" enableCopy="true" />** |
   | Password | **<inject key="AzureAdUserPassword" enableCopy="true" />** |

1. In the left navigation menu, under **Entra ID (1)**, select **Identity Secure Score (2)**.

   ![](./media/sc14.png)

1. On the **Security | Identity Secure Score**, review the information provided.

1. Notice the value to **Identity Secure Score**, your **Score History** and other information.

   ![](./media/sc15.png)

1. Scroll down to view the **Recommendations**.

   ![](./media/sc16.png)

    >**Note** - In contrast to the recommendations in Microsoft Defender for Cloud and Microsoft Defender XDR, these actions are specific to identity.  This provides a more focused list of potential actions to your security posture management for identity. Any recommendations initiated from this list will also provide an impact to your overall tenant security posture. 


### Task 2 - Execute an improvement action

In this task, you will execute an improvement action by enabling Microsoft Entra ID Identity Protection sign-in risk policies. You'll create a new conditional access policy to strengthen identity security, configuring users, resources, and access controls.

1. To improve one area of the identity security posture, select **Protect all users with a user risk policy**.

   ![](./media/sc17.png)

1. In the page that opens, review the risk. Additionally, you see an **Action plan** on how to resolve the threat.

1. Select the link **Follow these steps to create a Conditional Access policy from scratch or by using a template**. Review the steps in the article.

   ![](./media/sc18.png)

1. Close the article tab, and return to the tab with **Microsoft Entra ID** opened.

1. From the menu on the left, select **Conditional Access**.

   ![](./media/sc19.png)

1. Select **+ Create new policy**.

   ![](./media/sc20.png)

1. Use the following values to create the policy:

   - Name: **User risk protection policy (1)**

   - Assignments: Select **0 users or agents (Preview) selected (2)**

     ![](./media/sc21.png)

   - On the **Include (1)** tab mark **All users (2)**     

     ![](./media/sc22.png)

   -  On the **Exclude (1)** tab, use the **Users and groups (2)**  

     ![](./media/sc23.png)   

   - Choose any accounts that must maintain the ability to use legacy authentication. Microsoft recommends you exclude at least one account to prevent yourself from being locked out. For now select **Spektra Systems** and **ODL_User <inject key="DeploymentID"></inject> (3)** and then click **Select (2)**.

     ![](./media/sc24.png)  

   - Under Target resources, Select **No target resource selected (1)**, and then select **All resources (formerly 'All cloud apps') (2)**.

     ![](./media/sc25.png)

   - **Network:** Leave at default

   - Under Conditions select **0 conditions selected (1)** > Under **User risk** select the **Not configured (2)** link, set **Configure** to **Yes (3)**. Mark the box next to **High** and **Medium** **(4)** and then **Done (5)**.

     ![](./media/sc26.png)
   
   - **Access controls:**  Under **Grant** select **0 controls selected (1)**,Select **Require risk remediation (2)**

     ![](./media/sc27.png)

   - Under the **Require authentication strength** select **Phishing-resistant MFA (1)** and then **Select (2)**.

     ![](./media/sc28.png)

   - Confirm your settings and set Enable policy to **Report-only (1)**.

   - Select **Create (2)** to create to enable your policy.

     ![](./media/sc29.png)

## Review

In this lab, you have completed:
- Reviewed Identity Secure Score and improvement actions
- Executed an improvement action

## You have successfully completed the lab
