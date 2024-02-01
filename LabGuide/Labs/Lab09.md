## Lab 09 - Discover Apps 

## Lab scenario

Discovering Apps in the Microsoft 365 Defender suite involves gaining visibility into the applications used across an organization's digital environment. This process aims to comprehensively catalog and understand the landscape of applications, including cloud-based, on-premises, and third-party apps. By leveraging various tools and services within the suite, such as Microsoft Cloud App Security, administrators can identify and assess these applications for security risks, compliance adherence, and data usage patterns.

## Lab objectives (Duration: minutes)

In this lab, you will complete the following tasks:
- Task 1: Enable Defender for Endpoint integration
- Task 2: Configure the severity for alerts
- Task 3: Create a snapshot report

## Architecture Diagram

### Task 1: Enable Defender for Endpoint integration.


1. In [Microsoft Defender XDR](https://security.microsoft.com/), from the navigation pane, select **Settings** and then Select **Endpoints**.

   ![Picture 1](../Media/DiscoverApps 1.png)

2. Under General, select **Advanced features**. Toggle the Microsoft Defender for Cloud Apps to On. Select **Save preferences**.

   ![Picture 1](../Media/DiscoverApps 2.png)

### Task 2: Configure the severity for alerts.

1. In the Microsoft Defender Portal, select **Settings**. Then choose **Cloud Apps**. Under Cloud Discovery, select **Microsoft Defender for Endpoint**.

   ![Picture 1](../Media/DiscoverApps 3.png)

   ![Picture 1](../Media/DiscoverApps 4.png)

2. Under Alerts, select the global severity level for alerts.

   ![Picture 1](../Media/DiscoverApps 5.png)

3. Select **Save**.

### Task 3: Create a snapshot report.

1. Collect log files from your firewall and proxy, through which users in your organization access the Internet. Make sure to gather logs during times of peak traffic that are representative of all user activity in your organization.
2. In the Microsoft Defender Portal, under Cloud Apps, select **Cloud discovery**.

   ![Picture 1](../Media/DiscoverApps 6.png)

3. In the top-right corner, pull down Actions, and select **Create Cloud Discovery snapshot report**. Select **Next**.

   ![Picture 1](../Media/DiscoverApps 7.png)

4. Provide the details in the report details tab, Click on **Download sample log** which we will be using in next step and Select **Next**.
- **Report name** : Report<inject key="DeploymentID" enableCopy="false" /></inject>
- **Description** : New report
- **Source** : Blue coat ProxySG - Access log(W3C)

   ![Picture 1](../Media/DiscoverApps 9.png)

5. Select **Browse** and choose the source from which you want to upload the log files and select the sample log file which was downloaded in previous step. Select **Upload logs**.

   ![Picture 1](../Media/DiscoverApps 10.png)

> **Note**: Verify your log format to make sure that it's formatted properly according to the sample log you can download. Under Verify your log format, select View log format then select Download sample log. Compare your log with the sample provided to make sure it's compatible.

> **Note**: Verify your log format to make sure that it's formatted properly according to the sample log you can download. Upload traffic logs that you want to upload. You can upload up to 20 files at once. Compressed and zipped files are also supported.

9. Select **Settings**.Then under Cloud Discovery, select **Snapshot reports**, and select your snapshot report. You can see all the details regarding the report that you have uploaded.

   ![Picture 1](../Media/DiscoverApps 13.png)

10. Select Discovered apps to see all the apps present in the portal.

   ![Picture 1](../Media/DiscoverApps 15.png)

## Review
In this lab, you will complete the following tasks:
- Enable Defender for Endpoint integration
- Configure the severity for alerts
- Create a snapshot report
