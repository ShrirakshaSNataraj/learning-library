#  Configure Disposition Rule on MOU Records based on the event occurrence

## Introduction

In this lab,you will learn how to add event based disposition rule on MOU records that are no longer needed for the company.

### Objectives
* Workshop Overview
* Create Series , Retention Category and MOU record folder to store MOU documents.
* Add Disposition Rule on the Category for the MOU Record Folder based on the occurrence of the event.
* Check-in content item in the Record Folder.
* Disposition Processing on the record.

## Workshop Overview

In this workshop, you will understand the different types of disposition rules that can be applied on 3 different record folders shown in the diagram below.An Organization has legal documents that need to be categorized and stored in separate folders.Depending on its usage,records needs to be purged from the system that are no longer required. WebCenter Content Records Management provides various predefined events , retention periods and actions that can used according to the requirement.
   ![](./images/image%20(10).png " ")

There are 3 record folders each having legal records such as MOU's , Non-disclosure Agreement & Software Development Agreement all created under Retention Category named Legal Documents.For the MOU Record Folder ,event based disposition rule acts on the MOU records based on the occurrence of an event. After which the record gets closed or cut off and goes through the approval process before getting purged from the system .For the Non-disclosure Agreement Record Folder , time based disposition rule acts on the Agreements based on the certain time period the user has defined, followed by which the agreement gets archived or removed from the system. For the Software Agreement record folder,event-time based disposition rule acts on the Software Agreement based on both the occurrence of an event and at the certain time period defined by the user .Finally after the records in each specific records folder have met the condition and retained for certain time period,they are then purged from the system after the approval from the authorized user based on the configuration.

## Task 1: Create Retention Category and Records Folders


1.  Login to WebCenter Content Server.

2.  Click **Browse Content** then **Retention Schedules**.
.
    > **Note:** This page is only accessible after you install and configure Initial Record Settings shown in the Introduction.

3.  (Optional) Click on create **Series** (series is a logical container to hold any number of Retention Categories inside it) and give any logical name).


4.  On the Exploring Retention Schedule page, choose Create then Create Retention Category on the page menu.On the Create or Edit Retention Category page, enter the details as shown in the image below. 
    
    ![](./images/image%20(5).png " ")
    ![](./images/image%20(6).png " ")

5.  Click **Create**.

6. In the Legal Documents Retention Category Page, click on create records folder and create MOU records folder as shown below
     ![](./images/image%20(7).png " ")

7. Fill in the details as shown in the below image and click on Create button . Similarly create the other two records folders i.e Non-disclosure Agreement records folder to store Non-disclosure agreement records and Software Agreement Records Folder to store Software Agreement Records.
      ![](./images/image%20(8).png " ")
      ![](./images/image%20(4).png " ")

## Task 2: Add Disposition Rule on the Category for the MOU Record Folder.

1. In the row for the Legal Documents retention category on the Exploring Retention Schedule page, choose **Edit** then **Edit Disposition** from the item's Actions menu. 
    ![](./images/image%20(9).png " ")

2. In the Disposition Instructions area, click Add.

    > **Note:** The Category.Create right is required to perform this action. This right is assigned by default to the Records Administrator role.

3. On the Disposition Rule page, choose the disposition rule's triggering event from the Triggering Event (After) list.If the disposition rule has a retention period, enter an integer value for Retention Period (Wait for) and select the corresponding period from the Retention Period list.Select an action for the rule from the Disposition Action (Do) list.

4. When the MOU's are obsolete , delete all the revisions from the server.In the **After** list select Obsolete event and choose 0 retention period . In the **Action** list select Delete All Revisions (Destroy Metadata) action as shown in the image below.
   
 
5. Select the user to be notified.In the Advanced options select the Records Folder for the disposition rule to be applied.

     > **Note:** Creating User and assigning necessary roles and permissions to review records is shown in Lab 2.

    ![](./images/image%20(12).png " ")

6. Click on submit update to apply changes on the MOU Record Folder.
    ![](./images/image%20(13).png " ")

 You may now [proceed to the next lab](#next).


## Want to Learn More?

<!-- * [Setting Up Environment](https://otube.oracle.com/media/Setting+Up+GitHub/0_93stcjpb) -->
* [Defining and Processing Dispositions ](https://docs.oracle.com/middleware/12213/wcc/webcenter-content-manage/GUID-0827B335-BA5E-4B9C-9270-27BE4520391C.htm#WCCAA471)
<!-- * [Using GitHub Desktop to merge, commit and make pull requests](https://otube.oracle.com/media/t/1_bxj0cfqf) -->

## Acknowledgements

* **Authors:**
    * Shriraksha S Nataraj , Staff Solution Engineer , Oracle WebCenter Content
* **Contributors:**
    * Shriraksha S Nataraj , Staff Solution Engineer , Oracle WebCenter Content

* **Last Updated By/Date:** Shriraksha S Nataraj , May 2022
