---

copyright:
  years: 2023
lastupdated: "2023-10-23"

keywords: assigning access in openpages, IAM access for openpages, service roles in openpages, access policies in openpages

subcollection: openpages

---

{{site.data.keyword.attribute-definition-list}}

# User and group synchronization from {{site.data.keyword.Bluemix_notm}} to {{site.data.keyword.openpages_short}}
{: #iam-openpages-synchronization}

Users and groups that you create in {{site.data.keyword.Bluemix_notm}} are synchronized to {{site.data.keyword.openpages_short}}. Users are synchronized to {{site.data.keyword.openpages_short}} after they accept an invitation to join your account.
{: shortdesc}

A cron job synchronizes the users and groups from {{site.data.keyword.cloud}} to {{site.data.keyword.openpages_short}}. This synchronization process is a one-way operation.

When a user logs in to {{site.data.keyword.openpages_short}} for the first time, the user is added to the user and group registry in {{site.data.keyword.openpages_short}}. They do not need to wait for the synchronization job to run.

All the groups that are created in {{site.data.keyword.Bluemix_notm}} are created in {{site.data.keyword.openpages_short}} with the prefix `Cloud IAM -` added to the name of the group.

Users are assigned the profiles that are associated with their group. Administrators can associate groups to one or more profiles in {{site.data.keyword.openpages_short}}. If a user has no enabled profiles available, the fallback profile is used. The fallback profile allows a user who is either not associated with any profile, or whose profile is disabled or deleted, to log in to {{site.data.keyword.openpages_short}}.

In {{site.data.keyword.Bluemix_notm}}, if a user is assigned a role of {{site.data.keyword.openpages_short}} User, View, Operator, or Editor, either directly or indirectly through a group, the user can log in to {{site.data.keyword.openpages_short}} and has permission to access GRC data.

In {{site.data.keyword.Bluemix_notm}}, if a user is assigned a role of Administrator, either directly or indirectly through a
group, the user logs in to {{site.data.keyword.openpages_short}} as an administrator. {{site.data.keyword.openpages_short}} administrators are able to change locale, profiles, and roles directly from within {{site.data.keyword.openpages_short}}. These settings take precedence over settings in {{site.data.keyword.Bluemix_notm}} and are not overridden when a synchronization job runs.

If you create users in {{site.data.keyword.openpages_short}} directly, they are set to **Inactive**.
{: note}

## Properties that are overwritten in {{site.data.keyword.openpages_short}} by the user synchronization job
{: #properties-overwritten}

Because users and groups are synchronized from {{site.data.keyword.Bluemix_notm}}, if you change the following
properties in {{site.data.keyword.openpages_short}}, your changes are overwritten when the synchronization job runs.

### User properties
{: #user-properties}

- User Name
- First Name
- Last Name
- Email
- Description
- All fields in Password and Security Group properties

### Group properties
{: #group-properties}

- Description

If you add users to a group in {{site.data.keyword.openpages_short}}, and the group has a name that begins with `Cloud IAM –`, the synchronization job will remove those users from the group so that the list of users
in the group matches the list of users for the group in {{site.data.keyword.Bluemix_notm}}.
