# Set up Logrotate

## Introduction

This lab will guide you in setting up the logrotate utility on your host machine to periodically rotate the `usagetracker.log` generated by Java Usage Tracker.

Although the size of the Java Usage Tracker log file is small, you should consider periodically truncating, compressing, archiving, or deleting the log file. This is because the Java Usage Tracker does not check for available disk space or perform these administrative tasks on the log file as it incrementally adds records to it.

Estimated Time: 10 minutes

### Objectives

In this lab, you will:

* Set up logrotate on Linux instances

### Prerequisites

* Access to your host machine with management agent already setup
* Completed [Lab 1](?lab=set-up-oci-for-jms) to [Lab 7](?lab=install-management-agent-oca)

## Task 1: Set up logrotate on Linux instances

1. In the **Terminal** window, make sure Logrotate is installed.

    ```
    <copy>
    sudo yum install logrotate
    </copy>
    ```

2. Create a logrotate configuration file for JMS by entering this command.

    ```
    <copy>
    sudo nano /etc/logrotate.d/jms
    </copy>
    ```

3. In the file, paste the following text.

    ```
    <copy>
    /var/log/java/usagetracker.log {
      su mgmt_agent root
      create 666 mgmt_agent root
      rotate 5
      size 20M
      notifempty
      compress
      missingok
    }
    </copy>
    ```

4. To save the file, press **CTRL+x**. Before exiting, nano will ask you if you wish to save the file: Type **y** to save and exit, type **n** to abandon your changes and exit.

## Learn More

* Refer to [How to Create a Custom Log File Rotation by logrotate](https://support.oracle.com/knowledge/Oracle%20Linux%20and%20Virtualization/2087525_1.html) for more details.

* Use the [Troubleshooting](https://docs.oracle.com/en-us/iaas/jms/doc/troubleshooting.html#GUID-2D613C72-10F3-4905-A306-4F2673FB1CD3) chapter for explanations on how to diagnose and resolve common problems encountered when installing or using Java Management Service.

* If the problem still persists or if the problem you are facing is not listed, please refer to the [Getting Help and Contacting Support](https://docs.oracle.com/en-us/iaas/Content/GSG/Tasks/contactingsupport.htm) section or you may open a a support service request using the **Help** menu in the OCI console.

## Acknowledgements

* **Author** - Teck Kian Choo, Java Management Service
