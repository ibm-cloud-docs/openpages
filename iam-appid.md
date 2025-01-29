---

copyright:
  years: 2025
lastupdated: "2025-01-29"

keywords: IAM access for openpages, App ID, identity provider, IdP

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}


# Connecting to an external identity provider for authentication
{: #iam-appid}

You can connect your external identity provider to an {{site.data.keyword.cloud}} App ID instance, and then configure that App ID to connect directly to {{site.data.keyword.cloud}} Identity and Access Management (IAM) to federate authentication users of an enterprise to an {{site.data.keyword.cloud}} account.
{: shortdesc}


## Configuring App ID
{: #iam-appid-config}

To configure App ID, do the following steps:
1. Configure the integration by doing the steps in the following topic: [Configuring App ID with your identity provider](https://www.ibm.com/docs/en/watsonx/saas?topic=overview-configuring-app-id-your-identity-provider).

    The topic discusses watsonx, but the steps are the same for {{site.data.keyword.openpages_short}}.
    {: tip}

3. Get the URL for your identify provider.

   Click **Manage Access (IAM)**, and then click **Identity providers**.
   - If you have only one identity provider, copy the default URL.
   - If you have more than one identity provider, click the actions icon for the identify provider and click **View IdP URL**. Copy the URL.

2. Test the identity provider URL. Verify that your {{site.data.keyword.cloud}} dashboard is displayed.

## Onboarding users
{: #iam-appid-users}

Give the identity provider URL to your users. Ask them to log in by using the identity provider URL. After they log in successfully, they are added to {{site.data.keyword.cloud}} IAM.

Next, give the users access to {{site.data.keyword.openpages_short}}. For more information, see [Managing IAM access for {{site.data.keyword.openpages_short}}](/docs/openpages?topic=openpages-iam-openpage).

## Results
{: #iam-appid-result}

Users must now use the identity provider URL to access {{site.data.keyword.openpages_short}}.

The log in experience for users now follows these steps:
1. A user goes to the identity provider URL. The identity provider page is displayed.
2. The user authenticates with the identity provider. The user's {{site.data.keyword.cloud}} dashboard is displayed.
3. The user can access {{site.data.keyword.openpages_short}} through the **Resource List**. Alternatively, the user can create a bookmark.
