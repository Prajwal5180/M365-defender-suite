## Lab 03 - Configure Protection Policies

## Lab scenario

In this lab, you will Configure Anti-Spam, Anti-Malware, and Anti-Phishing policies in Microsoft Defender for Office 365 involves setting up rules to detect unwanted emails (spam), safeguard against malicious software (malware), and identify and block phishing attempts.

## Lab objectives (Duration: 50 minutes)

In this lab, you will complete the following tasks:
- Exercise 1: Configure Anti-Spam Policy
- Exercise 2: Configure Anti-malware Policy
- Exercise 3: Configure Anti-phishing Policy

## Architecture Diagram

   ![Picture 1](../Media/lab3-arch.png)

### Exercise 1: Configure Anti-Spam Policy

Anti-spam policies serve as the backbone for managing configurable settings related to spam filtering. These policies play a crucial role in filtering both incoming and outgoing emails, employing a diverse range of techniques such as content analysis and sender reputation checks to identify and prevent the transmission of spam. Anti-Spam policies are essential components in safeguarding your email communication against unwanted and potentially harmful spam. By configuring these policies, you gain control over the parameters that dictate how spam is identified and handled within your email environment.

1. Go to Microsoft Defender Portal at https://security.microsoft.com/.
2. Go to **Email and Collaboration** > **Policies & rules**> Select the **Threat policies**.
   
   ![Picture 1](../Media/1.png)

3. Under Policies Select the **Anti-spam**.

   ![Picture 1](../Media/2.png)
   
4. Select **Create Policy** > **Inbound**.

   ![Picture 1](../Media/4.png)

5. Under Name your policy tab provide **Name** : anti-spam and Description: anti-spam and select Next.

   ![Picture 1](../Media/5.png)

6. Under **Users, groups and domains** tab you will add the Users, Groups and Domains to be included in the Anti spam policy as depicted in the screenshot and select Next.

   ![Picture 1](../Media/antispams1.png)

   >**Note**: As we haven't created any groups so we will be configuring only Users and the domain for now. In the environment details tab you will get the username, the first part of the username will be the user & the second part will be the domain. Example, if the username is odl_user_1187266@azurehol1017.onmicrosoft.com, then the user would be **ODL_User 1187266**, while domain name would be **azurehol1017.onmicrosoft.com**.

7. Under Bulk email threshold & spam properties tab. Keep the default option selected and select Next. (The properties are customizable and can be adjusted to suit specific requirements)

   ![Picture 1](../Media/7-1.png)

8. Under Actions tab. Keep the default option selected and select Next.

   ![Picture 1](../Media/8-1.png)

9. Under Allow & block list tab. Select the **Manage 0 sender(s)** under **Senders(0)** in Blocked section to block the emails from sending emails. Manage blocked senders tab will open, select **+ Add senders**

   ![Picture 1](../Media/anti-spam-1.png)

10. A new tab **Add senders** will open. Provide your personal email address to verify whether the block is functioning correctly or not and select **Add senders**. Select **Done**.

    ![Picture 1](../Media/anti-spam-2.png)

    ![Picture 1](../Media/anti-spam-3.png)

11. You can see one sender is selected in the Blocked Senders section. Select **Next**.

    ![Picture 1](../Media/anti-spam-4.png)

10. Under Review tab. Select **Create** button.

    ![Picture 1](../Media/10.png)

11. Click on Done.

    ![Picture 1](../Media/as11.png)

12. Feel free to use the personal email address you provided in step 10 to send an email to the ODL_user email id: <inject key="AzureAdUserEmail"></inject> . You'll observe that the email is being filtered into the Junk Email folder.

### Exercise 2: Configure Anti-malware Policy

Anti-Malware policies are designed to safeguard against malware, viruses, spyware, and other harmful software that could be transmitted through emails. Anti-Malware policies scan incoming and outgoing emails for malicious content like malware and viruses. They use signature-based and behavior-based detection to identify threats, taking predefined actions upon detection, such as quarantining or deleting malicious attachments or links.

1. Go to Microsoft Defender Portal at https://security.microsoft.com/.
2. Go to **Email and Collaboration** > **Policies & rules**> Select the **Threat policies**.
   
   ![Picture 1](../Media/1.png)

3. Under Policies Select the **Anti-malware**.

   ![Picture 1](../Media/MALWARE3.png)

4. Select **Create** in Anti-malware tab.

   ![Picture 1](../Media/MALWARE4.png)

5. Under Name your policy tab provide **Name** : anti-malware and Description: Malware Policy and select Next.

   ![Picture 1](../Media/MALWARE5.png)

6. Under **Users and domains** tab add the Users, Groups and Domains to be included in the Anti malware policy and select Next.

   ![Picture 1](../Media/antimalwares1.png)

   >**Note**: As we haven't created any groups so we will be configuring only Users and the domain for now.In the environment details tab you will get the username, the first part of the username will be the user & the second part will be the domain. Example, if the username is odl_user_1187266@azurehol1017.onmicrosoft.com, then the user would be **ODL_User 1187266**, while domain name would be **azurehol1017.onmicrosoft.com**.

7. Under Protected settings tab, select **Select file types** to choose the file types which are automatically identified as malware in email messages. Type **.ps1** and select it. Select **Add** and **Done** button to add .ps1 file types as malware in the emails.

   ![Picture 1](../Media/malware-new-2.png)

8. In the Protected settings tab, select **Quarantine the message** under when these file types are found and select **Notify an admin about undelivered messages from internal senders** and **Notify an admin about undelivered messages from internal senders** and provide the ODL_user email id: <inject key="AzureAdUserEmail"></inject> in both section and select **Next**.

   ![Picture 1](../Media/malware-new-1.png)

8. Under Review tab. Click on Submit button.

   ![Picture 1](../Media/MALWARE8.png)

9. Click on Done.
    
    ![Picture 1](../Media/am9.png)

12. Feel free to use your personal email address to send an email to the ODL_user email id: <inject key="AzureAdUserEmail"></inject> with any of the file types mentioned in the protection settings but for now you can add any file with type **.ps1** extension and send the email. You'll receive one email with the title **Undeliverable message** with the message **Your email message was not delivered to the intended recipients because malware was detected.**.

    ![Picture 1](../Media/malware-new-4.png)

### Exercise 3: Configure Anti-phishing Policy

Anti-phishing in Microsoft Defender for Office 365 is a comprehensive security feature designed to protect against phishing attacks within emails. Anti-phishing feature works by continuously scanning incoming emails in real-time, employing techniques like suspicious URLs and content analysis to detect potential phishing threats.

1. Go to Microsoft Defender Portal at https://security.microsoft.com/.
2. Go to **Email and Collaboration** > **Policies & rules**> Select the **Threat policies**.
   
   ![Picture 1](../Media/1.png)

3. Under Policies Select the **Anti-phishing**.

4. Under policy name tab provide **Name** : anti-phishing and Description: anti phishing and select Next.

   ![Picture 1](../Media/PHISHING1.png)

5. Under **Users, groups and domains** tab add the Users, Groups and Domains to be included in the Anti phishing policy and select Next.

   ![Picture 1](../Media/antiphishings1.png)

   >**Note**: As we haven't created any groups so we will be configuring only Users and the domain for now.In the environment details tab you will get the username, the first part of the username will be the user & the second part will be the domain. Example, if the username is odl_user_1187266@azurehol1017.onmicrosoft.com, then the user would be **ODL_User 1187266**, while domain name would be **azurehol1017.onmicrosoft.com**.

6. Under Phishing threshold & protection tab, keep the Phishing email threshold as **1- Standard**. Under **Impersonation**, select the checkbox **Enable users to protect** and select **manage 0 sender(s)** to add the senders to be included in phishing protection. A new tab **Manage senders for impersonation protection** will open, select **Add user**. A new tab **Add user** will open, provide a name and valid email address. You can provide your personal email address or any specific email address that you want to configure in this policy. Then, click on **Add**.
You will be back in the Manage senders for impersonation protection tab, you can see the user that you have added then click on **Done**.

   ![Picture 1](../Media/phishing-new-1.png)

   ![Picture 1](../Media/phishing-new-4.png)

   ![Picture 1](../Media/phishing-new-5.png)

7.  Under Phishing threshold & protection tab, select the checkbox **Enable domains to protect** and **Include domains I own** to enable impersonation protection for you domain. You can also select **Include custom domains** and manage domains that could be yours or domains that belong to your key suppliers and partners.

     ![Picture 1](../Media/phishing-new-7.png)


7. Under Phishing threshold & protection tab, select the checkbox **Manage 0 trusted sender(s) and domain(s)**. A new tab **Manage custom domains for impersonation protection** will open. Keep the **Sender** option selected, select **Add senders** and provide the email that you want to keep exceptions to the impersonation protection settings and select **Add**.

   ![Picture 1](../Media/phishing-new-8.png)

   ![Picture 1](../Media/phishing-new-9.png)

8. In the **Manage custom domains for impersonation protection** tab, select **Domain>Add domains**. A new tab **Add trusted domains** will open, provide the domain that you want to keep exceptions to the impersonation protection settings and select **Add**.

   ![Picture 1](../Media/phishing-new-10.png)

   ![Picture 1](../Media/phishing-new-11.png)


7. Under Actions tab, keep the default options selected and click on Next.

   ![Picture 1](../Media/ps8.png)

8. Under Review tab, click on Submit button.

   ![Picture 1](../Media/PHISHING9.png)

9. Click on Done.

   ![Picture 1](../Media/ps10.png)

10. From the left panel select **Review** under Email & collaboration. You'll observe the presence of four segments, as **Action center**, **Quarantine**, **Restricted Entities**, **Malware trends**. You have the option to choose these and respond to the threats that have occurred to the user.

    ![Picture 1](../Media/phishing-new-12.png)

11. Select **Quarantine** tab. You will be redirected to Quarantine page. Select **Email** tab if not selected. You'll find a list of emails that have been placed in quarantine based on the policy we've established. Select any of the email, it will open a new tab with all the details of email. You can select **Release email** to release it from qurantine to the recipient of the email.

    ![Picture 1](../Media/phishing-new-13.png)

12. A new tab **Release email to recipients inboxes** will open. Select **Release to all recipients** to release the email for all respective recipients and select **Release message**.

    ![Picture 1](../Media/phishing-new-14.png)

13. You will notice the successful message **Email has been released to recipient inboxes**. Click **Done**, and then you can verify the recipient's inboxes to ensure the email reaches its intended destination.

    ![Picture 1](../Media/phishing-new-15.png)
 
## Review
In this lab, you will complete the following tasks:
- Configured Anti-Spam Policy
- Configured Anti-malware Policy
- Configured Anti-phishing Policy
