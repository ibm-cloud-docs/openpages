---

copyright:
  years: 2023
lastupdated: "2023-10-14"

keywords: assigning access in openpages, IAM access for openpages, service roles in openpages, access policies in openpages

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}


# User and group synchronization from {{site.data.keyword.Bluemix_notm}} to {{site.data.keyword.openpages_short}}
{: #iam-openpages-synchronization}

Users and groups that you create in {{site.data.keyword.Bluemix_notm}} are synchronized to {{site.data.keyword.openpages_short}}. Users are
synchronized to {{site.data.keyword.openpages_short}} after they accept an invitation to join your account.
{: shortdesc}

All the groups that are created in {{site.data.keyword.Bluemix_notm}} are created in {{site.data.keyword.openpages_short}} with the prefix "Cloud
IAM -" added to the name of the group.

Users are assigned the profiles that are associated with their group. Administrators can
associate groups to one or more profiles in {{site.data.keyword.openpages_short}}. If a user has no enabled profiles
available, the fallback profile is used. The fallback profile allows a user who is either not
associated with any profile, or whose profile is disabled or deleted, to log in to {{site.data.keyword.openpages_short}}.

In {{site.data.keyword.Bluemix_notm}}, if a user is assigned a role of {{site.data.keyword.openpages_short}} User, View, Operator, or Editor, either
directly or indirectly through a group, the user can log in to {{site.data.keyword.openpages_short}} and has permission to
access GRC data.

In {{site.data.keyword.Bluemix_notm}}, if a user is assigned a role of Administrator, either directly or indirectly through a
group, the user logs in to {{site.data.keyword.openpages_short}} as an administrator. {{site.data.keyword.openpages_short}} administrators are able to
change locale, profiles, and roles directly from within {{site.data.keyword.openpages_short}}. These settings take
precedence over settings in IBM Cloud and are not overridden when a synchronization job runs.

Note: If you create users in {{site.data.keyword.openpages_short}} directly, they are set to **Inactive**.

## Properties that are overwritten in {{site.data.keyword.openpages_short}} by the user synchronization job

Because users and groups are synchronized from {{site.data.keyword.Bluemix_notm}}, if you change the following
properties in {{site.data.keyword.openpages_short}}, your changes are overwritten when the synchronization job runs.

### User properties

- User Name
- First Name
- Last Name
- Email
- Description
- All fields in Password and Security Group properties

### Group properties

- Description

If you add users to a group in OpenPages, and the group has a name that begins with "Cloud
IAM – ", the synchronization job will remove those users from the group so that the list of users
in the group matches the list of users for the group in {{site.data.keyword.Bluemix_notm}}.

## Adding and changing users and groups

The following scenarios show what happens when you create and modify users and groups.

### Creating a non-administrator group 

**Action in {{site.data.keyword.Bluemix_notm}}**

Create a group with the following settings:
- Service: {{site.data.keyword.openpages_short}}
- Resources: An {{site.data.keyword.openpages_short}} service
- Roles and actions: {{site.data.keyword.openpages_short}} User, Viewer, Editor, or Operator
   
**Outcome in {{site.data.keyword.openpages_short}}** 

If the group has users, it is created with the name and description you specified in IBM Cloud.
   
The group name is always prefixed by "Cloud IAM – " and is a subgroup under the "Workflow, Reporting and Others" group. Existing users that are added to the group in {{site.data.keyword.Bluemix_notm}} IAM are associated with the group in {{site.data.keyword.openpages_short}}.

### Creating a administrator group 

**Action in {{site.data.keyword.Bluemix_notm}}**

Create a group with the following settings:
- Service: {{site.data.keyword.openpages_short}}
- Resources: An {{site.data.keyword.openpages_short}} service
- Roles and actions: Administrator

**Outcome in {{site.data.keyword.openpages_short}}** 

If the group has users, it is created with the name and description you specified in {{site.data.keyword.Bluemix_notm}}. The group name is always prefixed by "Cloud IAM - " and is a subgroup under "Workflow, Reporting and Others" group.

Existing users that are added to the group in {{site.data.keyword.Bluemix_notm}}
IAM are members of the group in {{site.data.keyword.openpages_short}} and the
OPAdministrators group. As members of the OPAdministrators group, users have administrative privileges in {{site.data.keyword.openpages_short}}.

### Creating a non-administrator user 

**Action in {{site.data.keyword.Bluemix_notm}}**

Create a user with the following settings:
- Service: {{site.data.keyword.openpages_short}}
- Resources: An {{site.data.keyword.openpages_short}} service
- Roles and actions: {{site.data.keyword.openpages_short}} User, Viewer, Editor, or Operator

**Outcome in {{site.data.keyword.openpages_short}}** 

In {{site.data.keyword.openpages_short}}, the user is not a member of any groups by default.

The user is created with the User Name, Display Name, Email, and Group associations that you specified in {{site.data.keyword.Bluemix_notm}}.

The locale is U.S. English. In {{site.data.keyword.openpages_short}}, users and administrators can change a user’s locale. The synchronization job does not overwrite an existing user’s locale.

Users are assigned allowed profiles through their group associations. If a user has multiple allowed profiles, a preferred profile selection panel is displayed when the user logs in to {{site.data.keyword.openpages_short}} for the first time.

When a user has no other enabled profiles available, a fallback profile is used. A fallback profile allows a user who is either not associated with any profile, or whose profile is disabled or deleted, to log in to OpenPages.

When you are provisioning the service, you select the solutions you want from a list. The first solution you selected on the list determines which master profile is used as the fallback profile. For example, if you select the Business Continuity Management (BCM) and Financial Controls Management (FCM) solutions when you provisioned the service, the BCM Master profile is the fallback profile.

Users are assigned role templates through their group associations.