#  Get Started with Records Disposition Program with WebCenter Content:Records 

## Introduction

In this lab, you will learn how to configure the Records Management System in WebCenter Content and also set up the initial set up checklist.

### Objectives
* Start WebLogic and WebCenter Content Server.
* Selecting the Installation option for Records.
* Configure Setup Checklist.


## Task 1: Start WebLogic and WebCenter Content Server

Before getting started, you should start the WebLogic server and content server.

1.  Login to the demo environment. Navigate to the following directory shown below and run the command startWebLogic.cmd .
       ```
    <copy>C:\Oracle\Middleware\Oracle_Home\user_projects\domains\base_domain\bin</copy>
    ```

2.  Once the WebLogic is running,start the content server using the same location mentioned above and start UCM server    with the command startManagedWebLogic.cmd UCM_server1 to start the WebCenter Content Server.
    > **Note:** Make sure to login to the database and check if the pluggable database PDBORCL is in read/write mode before starting the servers.

3. Open any browser and type the following URL to access the WebCenter Content Server.
   http://localhost:16200/cs/


## Task 2: Install Records on UCM and configure the Setup Checklist.


1. Login to Content server as an administrator and click on **Configure Records Settings** under Administration tab as shown in the image below.
    ![](./images/image.png " ")

2.  Select the software configuration as shown in the image . 
      ![](./images/image%20(1).png " ")
 
    > **Note:** Restart the servers after selecting the installation settings for the changes to be applied.
  

3. After the installation is successfully completed ,configure the setup checklist by clicking on **Records** tab,select **Configure** option and then select **Setup Checklist**.
     ![](./images/Screenshot%20(3).png " ")

4. On the Setup Checklist page install the defaults and configure security settings.
     ![](./images/image%20(3).png " ") 


This concludes this lab. You may now proceed to the next lab.

## Want to Learn More?

<!-- * [Setting Up Environment](https://otube.oracle.com/media/Setting+Up+GitHub/0_93stcjpb) -->
* [Download and Install Git for Windows and Mac](https://git-scm.com/download/win)
<!-- * [Using GitHub Desktop to merge, commit and make pull requests](https://otube.oracle.com/media/t/1_bxj0cfqf) -->

## Acknowledgements

* **Authors:**
    * Shriraksha S Nataraj, Staff Solution Engineer , Oracle WebCenter Content
* **Contributors:**
    * Shriraksha S Nataraj, Staff Solution Engineer , Oracle WebCenter Content
* **Last Updated By/Date:** Shriraksha S Nataraj , April 2022
