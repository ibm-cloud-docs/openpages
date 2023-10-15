---

copyright:
  years: 2023
lastupdated: "2023-10-12"

keywords: adding users in openpages, inviting users in openpages

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}


# Adding users to your {{site.data.keyword.openpages_short}} instance
{: #iam-adding_users}

After you provision your service instance of {{site.data.keyword.openpages_short}}, you can invite additional users to access it.
{: shortdesc}

You can also create access groups. For more information, see [Setting up access groups](/docs/account?topic=account-groups&interface=ui).

The provisioning process requires two steps: 
1. Invite users to your {{site.data.keyword.Bluemix_notm}} account by using IAM. 
2. Grant the users access within {{site.data.keyword.openpages_short}}.

To learn more about IBM Cloud Identity and Access Management (IAM), see [the IAM overview](/docs/account?topic=account-iamoverview) or the [Best practices for assigning access](/docs/account?topic=account-account_setup).
{: tip}

To invite users to your {{site.data.keyword.Bluemix_notm}} account, do the following steps:
1. In the {{site.data.keyword.Bluemix_notm}} menu bar, click **Manage** > **Access (IAM)**.
2. Click **Invite Users**.
3. Enter the users’ email addresses into the text box.
4. Configure the users’ access policy.
   - Click **Access Policy**.
   - In the search field of the **Service** section, type **openpages** and select **IBM OpenPages**.
   - Click **Next**.
   - Click **All resources**, and then click **Next**.

   Alternatively, if you have multiple instances, you can grant access to a specific one. Click **Specific resources**, and then select an {{site.data.keyword.openpages_short}} instance.
5. Under Service access, do one of the following steps:
   - To set up the user as an {{site.data.keyword.openpages_short}} administrator, under **Platform access**, select **Administrator**.
   - To set up a non-admin user, click **OpenPages User** and do not select a platform access role.

   Non-admin users get login access only. You need to assign them profiles and role templates in {{site.data.keyword.openpages_short}}. You can do this after you add the user in {{site.data.keyword.Bluemix_notm}}. 
6. Click **Review** and verify your updates.
7. Click **Add**. The **Access summary** panel shows the policy that you created.
8. Click **Invite**. The users that you selected receive an email from `noreply <no-reply@cloud.ibm.com>`, inviting them to access your {{site.data.keyword.Bluemix_notm}} account. Users need to accept this invitation before they can access the {{site.data.keyword.openpages_short}} instance.


