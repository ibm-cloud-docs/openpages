---

copyright:
  years: 2026
lastupdated: "2026-03-26"

keywords: IAM access for openpages, App ID, identity provider, IdP

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}


# Connecting to an external identity provider for authentication
{: #iam-external-identity-provider}

IBM Cloud service offers multiple external identity provider integration options. For more information, see [Which is the right federation option for you?](https://cloud.ibm.com/docs/account?topic=account-federation-option-for-you). This topic describes the option of using IBM Cloud SAML service provider (SP) as well as App ID to connect to an external identify provider.

## Configuring IBM Cloud SAML service provider (SP) and IAM to use single sign-on (SSO)
{: #iam-saml-config}

You can integrate with your external identity provider (IdP) to securely authenticate external users to your {{site.data.keyword.cloud}}. By using your IdP, you can provide a way for users in your company to use single sign-on (SSO). You can connect your cloud account to an external IdP by using the {{site.data.keyword.Bluemix_notm}} SAML service provider (SP).

To configure IBM Cloud SAML service provider (SP), do the following steps:
1. Configure the integration by doing the steps in the following topic: [Federating with the IBM Cloud SAML service provider (SP)](https://cloud.ibm.com/docs/account?topic=account-ibm-idp-integration#federate-cloud-saml).

2. Get the Realm ID for your identity provider.

    Click **Manage Access (IAM)**, and then click **Identity providers**. Identify your provider, click to open the detail page and copy the Realm ID.

3. Ensure that you have an {{site.data.keyword.openpages_short}} instance. If you need to create an {{site.data.keyword.openpages_short}} instance, see [Provisioning your IBM OpenPages as a Service environment](/docs/openpages?topic=openpages-provisioning_environment).

    You can integrate more than one {{site.data.keyword.openpages_short}} instance in this account with the same Custom identity provider.

    Open a support case for each {{site.data.keyword.openpages_short}} instance requesting for the Custom identity provider integration and include the {{site.data.keyword.openpages_short}} instance CRN and Realm ID that you copied from the previous step in the case. For more information on creating the case, see [Creating support cases](/docs/account?topic=account-open-case).

    After the support case is addressed from the {{site.data.keyword.Bluemix_notm}} team and is closed, the Custom identity provider integration for the provided {{site.data.keyword.openpages_short}} instance CRN is completed.

## Onboarding users
{: #iam-saml-users}

The following options are available to give users access to {{site.data.keyword.openpages_short}}:

- Configure [dynamic rules](https://cloud.ibm.com/docs/account?topic=account-rules&interface=ui) to automatically assign users to an access group where the {{site.data.keyword.openpages_short}} access is granted by an {{site.data.keyword.Bluemix_notm}} IAM role, and where the role templates from {{site.data.keyword.openpages_short}} is assigned.
- When users login to the {{site.data.keyword.openpages_short}} instance successfully, they are added to {{site.data.keyword.Bluemix_notm}} IAM. Next, give the users access to {{site.data.keyword.openpages_short}}. For more information, see [Managing IAM access for IBM OpenPages](https://cloud.ibm.com/docs/openpages?topic=openpages-iam-openpages&interface=ui).

## Results
{: #iam-saml-result}

1. For users to access their {{site.data.keyword.openpages_short}} instance, they must follow the steps in the [{{site.data.keyword.openpages_short}} UI](https://cloud.ibm.com/docs/openpages?topic=openpages-log_in#method1).
2. When the user launches their {{site.data.keyword.openpages_short}} instance, they are redirected for authentication to their Custom identity provider and after successful authentication, the users are logged into {{site.data.keyword.openpages_short}}.

## Configuring trusted profile
{: #iam-saml-trusted-profile}

1. By using trusted profiles, federated users can be given conditional access management to establish a flexible, secure way to access the {{site.data.keyword.openpages_short}} resources to do their job. Users must follow the setps to configure the same [Managing access for federated users by using trusted profiles](https://cloud.ibm.com/docs/account?topic=account-trustedprofile-fedusers-tutorial&interface=ui).

## Configuring App ID and IAM
{: #iam-appid-config}

You can connect your external identity provider to an {{site.data.keyword.cloud}} App ID instance, and then configure that App ID to connect directly to {{site.data.keyword.cloud}} Identity and Access Management (IAM) to federate authentication users of an enterprise to an {{site.data.keyword.cloud}} account.
{: shortdesc}

To configure App ID, do the following steps:
1. Configure the integration by doing the steps in the following topic: [Configuring App ID with your identity provider](https://www.ibm.com/docs/en/watsonx/saas?topic=overview-configuring-app-id-your-identity-provider).

    The topic discusses watsonx, but the steps are the same for {{site.data.keyword.openpages_short}}.
    {: tip}

2. Get the Realm ID for your identity provider.

    Click **Manage Access (IAM)**, and then click **Identity providers**. Identify your provider, and copy the Realm ID.

3. Ensure that you have an {{site.data.keyword.openpages_short}} instance. If you need to create an {{site.data.keyword.openpages_short}} instance, see [Provisioning your IBM OpenPages as a Service environment](/docs/openpages?topic=openpages-provisioning_environment).

    You can integrate more than one {{site.data.keyword.openpages_short}} instance in this account with the same Custom identity provider.

    Open a support case for each {{site.data.keyword.openpages_short}} instance requesting for the Custom identity provider integration and include the {{site.data.keyword.openpages_short}} instance CRN and Realm ID that you copied from the previous step in the case. For more information on creating the case, see [Creating support cases](/docs/account?topic=account-open-case).

    After the support case is addressed from the {{site.data.keyword.Bluemix_notm}} team and is closed, the Custom identity provider integration for the provided {{site.data.keyword.openpages_short}} instance CRN is completed.

## Onboarding users
{: #iam-appid-users}

The following options are available to give users access to {{site.data.keyword.openpages_short}}:

- Configure [dynamic rules](https://cloud.ibm.com/docs/account?topic=account-rules&interface=ui) to automatically assign users to an access group where the {{site.data.keyword.openpages_short}} access is granted by an {{site.data.keyword.Bluemix_notm}} IAM role, and where the role templates from {{site.data.keyword.openpages_short}} is assigned.
- When users login to the {{site.data.keyword.openpages_short}} instance successfully, they are added to {{site.data.keyword.Bluemix_notm}} IAM. Next, give the users access to {{site.data.keyword.openpages_short}}. For more information, see [Managing IAM access for IBM OpenPages](https://cloud.ibm.com/docs/openpages?topic=openpages-iam-openpages&interface=ui).

## Results
{: #iam-appid-result}

1. For users to access their {{site.data.keyword.openpages_short}} instance, they must follow the steps in the [{{site.data.keyword.openpages_short}} UI](https://cloud.ibm.com/docs/openpages?topic=openpages-log_in#method1).
2. When the user launches their {{site.data.keyword.openpages_short}} instance, they are redirected for authentication to their Custom identity provider and after successful authentication, the users are logged into {{site.data.keyword.openpages_short}}.
