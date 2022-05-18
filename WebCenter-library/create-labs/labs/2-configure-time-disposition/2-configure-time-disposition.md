# Time Based Disposition Example using Custom Trigger

## Introduction

This lab explains how to configure custom triggers and use time based disposition rule on the Non-Disclosure Record Folder.

### Objectives

* Create Custom Trigger.
* Add disposition Rule on Non-Disclosure Agreement Record Folder.
* Create User and add record reviewer roles.

## Task 1: Create Custom Trigger

Global triggers have an activation date. The activation date can be a past, present, or future date. A user can create a trigger and delay the activation of a trigger for an indefinite amount of time until activation is required. In essence this is a dormant trigger, which does not contain an activation date.

A user can create a trigger that activates immediately, activate a trigger on a certain date and time, or delay the activation of a trigger for an indefinite amount of time until activation is required.

1. Choose Records then Configure from the Top menu. Choose Retention then Triggers from the Page menu.The Configure Triggers Page opens.

   ![](./images/image%20(14).png " ")

2. Select the type of trigger to create (Global, Custom Direct, or Indirect). Choose Add.The Create or Edit Trigger Type Page opens.Enter an Activation Date. If not entered it is considered a dormant trigger, which can be activated later.

   ![](./images/image%20(15).png " ")

3. As shown in the image above,enter the trigger name as **Year End** and the activation date.Click on Create.


## Task 2: Add disposition Rule on Non-Disclosure Agreement Record Folder
  
  1. In the Retention Category Page , Click on Edit Disposition for Legal Documents Category . 
  
  2. Click on **Add** to add another disposition rule . From the After list select the custom trigger Year end from the list and for the retention period field select Months and give the integer value as 6.In the Do list select Expire and for the notification reviewer field select the user Mark for reviewing the record before disposition to act.
   
     ![](./images/image%20(16).png " ")

  3. In the Advanced Section ,select the records folder Non-disclosure Agreement and click on Ok.

  4. Click on **Submit Update** to apply changes on the Non-disclosure Agreement Record folder. 

## Task 3: Create User and add record reviewer roles

  1. User with admin role can create Users and assign necessary Roles.Go to **Administration** tab and select **Admin Applets**

  2. Run the **User Admin** applet and click on **Add** to create the user. Add the details as shown in the image below. And go to **Roles** add rma,rmadmin role to the user .
     ![](./images/image%20(19).png " ")
     ![](./images/image%20(20).png " ")

  3. In the main menu , Click on Aliases and select RmaReviewers.Add the user Mark by clicking on the **Add** option. 
      ![](./images/image%20(21).png " ")

This concludes this lab. You may now proceed to the next lab.


## Acknowledgements

* **Author:**
    * Shriraksha S Nataraj, Staff Solution Engineer, Oracle WebCenter Content
* **Contributors:**
    * Shriraksha S Nataraj , Staff Solution Engineer , Oracle WebCenter Content

* **Last Updated By/Date:** Shriraksha S Nataraj ,May 2022
