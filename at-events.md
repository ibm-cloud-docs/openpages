---

copyright:
  years: 2025
lastupdated: "2025-07-28"

keywords: audit events in openpages, audit activity in openpages

subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Auditing events for {{site.data.keyword.openpages_short}}
{: #at_events}

As a security officer, auditor, or manager, you can use the {{site.data.keyword.logs_full_notm}} service to track how users and applications interact with the {{site.data.keyword.openpages_short}} service in {{site.data.keyword.cloud_notm}}.
{: shortdesc}

{{site.data.keyword.logs_full_notm}} records user-initiated activities that change the state of a service in {{site.data.keyword.cloud_notm}}. You can use this service to investigate abnormal activity and critical actions and to comply with regulatory audit requirements. In addition, you can be alerted about actions as they happen. The events that are collected comply with the Cloud Auditing Data Federation (CADF) standard. For more information, see [Getting started with {{site.data.keyword.logs_full_notm}}](/docs/cloud-logs?topic=cloud-logs-getting-started).

The same instance of {{site.data.keyword.logs_full_notm}} service can be used for [OpenPages Platform Logging](/docs/openpages?topic=openpages-logging) purposes.

## List of platform events
{: #at_actions_platform}


The following table lists the actions on service instances that generate an event:

| Action                                       | Description |
| -------------------------------------------- | ----------- |
| `openpages.service.get` | An event is generated when service instance details are displayed in the Console UI.  |
| `openpages.service-status.disable` | An event is generated when a service instance is disabled. For example, when an instance is deleted in the Console UI, the instance is disabled. |
| `openpages.service-status.enable` | An event is generated when a service instance is enabled. For example, when an instance is restored by reclamation, the instance is enabled. |
| `openpages.service.restore` | An event is generated when a service instance is restored from a source instance. |
| `openpages.service-aifactsheets-configuration.get` | An event is generated when the configuration for watsonx.governance is fetched. |
| `openpages.service-user-metrics.get` | An event is generated when user metrics are retrieved and displayed on the **Usage** tab in the Console UI.  |
| `openpages.service.delete` | An event is generated when an instance is deleted.  |
| `openpages.service.configure` | An event is generated when a service instance configuration is started. |
| `openpages.service-allow-list.update` | An event is generated when the allow list for an instance is updated in the Console UI. |
| `openpages.service-host-transfer.start` | An event is generated when you transfer a custom host name to another instance in the Console UI. |
| `openpages.service-readiops-metrics.get` | An event is generated when database read IOPS metrics are fetched. |
| `openpages.service-writeiops-metrics.get` | An event is generated when database read IOPS metrics are fetched. |
| `openpages.service-filter.list` | An event is generated when the list of service instances in the Console UI is filtered.  |
| `openpages.service.update` | An event is generated when an instance is updated.  |
| `openpages.service.add` | An event is generated when an instance is provisioned.  |
| `openpages.service-aifactsheets-configuration.delete` | An event is generated when the configuration for watsonx.governance is deleted. |
| `openpages.service-restorable-instant.get` | An event is generated when the oldest restorable timestamp of the service instance is fetched. |
| `openpages.service-upgrade.start` | An event is generated when a service instance is upgraded. |
| `openpages.service-aifactsheets-configuration-validation.evaluate` | An event is generated when the configuration for watsonx.governance is validated. |
| `openpages.services-promoted-component-version.get` | An event is generated when the most recently promoted version of a service instance is fetched. |
| `openpages.service-aifactsheets-configuration.update` | An event is generated when the configuration for watsonx.governance is updated. |
| `openpages.service-eventnotification.update` | An event is generated when the event notification settings for an instance are modified in the Console UI.  |
| `openpages.service-cpu-metrics.get` | An event is generated when service CPU metrics are fetched. |
| `openpages.service-solution-usage.update` | An event is generated when the solution configuration for a service instance is updated.  |
| `openpages.service-custom-resource.renew` | An event is generated when a service instance is patched.  |
| `openpages.service-storage-metrics.get` | An event is generated when storage metrics are retrieved and displayed on the **Usage** tab in the Console UI.  |
| `openpages.service.list` | An event is generated when the list of service instances is displayed in the Console UI.  |
{: caption="Actions that generate platform events (UI)" caption-side="bottom"}

## Users, groups, login, and logout events
{: #users-groups}

The following tables list events that are generated when users log in, users log out, and when user management actions occur.

Login, Logout, Session, Authentication:

| Action:                         | Description:                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------ |
| `openpages.user.logoff`         | An event is generated when a user logs out of {{site.data.keyword.openpages_short}}. |
| `openpages.user.logon`          | An event is generated when a user logs in to {{site.data.keyword.openpages_short}}.  |
| `openpages.user.session-expire` | An event is generated when a user session expires.                                   |
{: caption="Actions that generate login, logout, session authentication events (UI)" caption-side="bottom"}


User Management:

| Action:                                 | Description:                                                          |
| --------------------------------------- | --------------------------------------------------------------------- |
| `openpages.user-lock.set-off` | An event is generated when a user account is unlocked. |
| `openpages.user.disable` | An event is generated when a user account is disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `true` and `newValue` is set to `false`, the user account is disabled. |
| `openpages.user.create` | An event is generated when a user is created. |
| `openpages.user-password.update` | An event is generated when a user password is modified. |
| `openpages.user-current-profile.update` | An event is generated when a user switches profiles in {{site.data.keyword.openpages_short}}. |
| `openpages.user-lock.set-on` | An event is generated when a user account is locked. |
| `openpages.user-locale.update` | An event is generated when a user switches locales in {{site.data.keyword.openpages_short}}. |
| `openpages.user-preference.set` | An event is generated when a user preference is set. |
| `openpages.user-membership.list` | An event is generated when a list of user group memberships is fetched. |
| `openpages.user.enable` | An event is generated when a user account is enabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the user account is enabled. |
| `openpages.user.get` | An event is generated when a user is fetched. |
| `openpages.user.list` | An event is generated when a list of users is fetched. |
| `openpages.user.update` | An event is generated when a user  is modified. |
{: caption="Actions that generate user management events (UI)" caption-side="bottom"}


Group Management:

| Action:                                         | Description:                                                                                       |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `openpages.group.get` | An event is generated when a group is fetched. |
| `openpages.group-profile.remove` | An event is generated when object profiles are dissociated from a group. |
| `openpages.group-profile.add` | An event is generated when object profiles are associated to a group. |
| `openpages.group-administrator-permission.allow` | An event is generated when administrative permissions are granted to a group. |
| `openpages.group.create` | An event is generated when a group is created. |
| `openpages.group-member.delete` | An event is generated when a user is removed from a group. |
| `openpages.group.list` | An event is generated when a list of groups is fetched. |
| `openpages.group-administrator-permission.update` | An event is generated when the administrative permissions that are assigned to a group are modified. |
| `openpages.group-member.update` | An event is generated when members are updated for a group. |
| `openpages.group-permission.update` | An event is generated when the permissions that are assigned to a group are modified. |
| `openpages.group.update` | An event is generated when a group is updated. |
| `openpages.group-administrator-permission.revoke` | An event is generated when administrative permissions are revoked from a group. |
| `openpages.group-member.add` | An event is generated when users are added to a group. |
{: caption="Actions that generate group management events (UI)" caption-side="bottom"}

## System administration and security events
{: #system-admin}

Audit trail:

| Action:                            | Description:                                                             |
| ---------------------------------- | ------------------------------------------------------------------------ |
| `openpages.resource-activity.list` | An event is generated when a list of changes to an object is displayed on the Activity tab. |
| `openpages.resource-activity.get` | An event is generated when a change to an object is displayed on the Activity tab. |
| `openpages.resource-activity.export` |  |
{: caption="Actions that generate audit trail events (UI)" caption-side="bottom"}

Currencies:

| Action:                           | Description:                                                             |
| --------------------------------- | ----------------------------------------------------------------------   |
| `openpages.currency.upload` | An event is generated when a currency is uploaded. |
| `openpages.currency.list` | An event is generated when a list of currencies is fetched. |
| `openpages.currency.update` | An event is generated when a currency is updated. |
| `openpages.currency.disable` | An event is generated when a currency is disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `true` and `newValue` is set to `false`, the currency is disabled. |
| `openpages.currency.enable` | An event is generated when a currency is enabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the currency is enabled. |
{: caption="Actions that generate currency events (UI)" caption-side="bottom"}



Encryption keystore:

| Action:                                 | Description:                                             |
| --------------------------------------- | -------------------------------------------------------- |
| `openpages.encryption-keystore.disable` | An event is generated when an encryption key is disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the encryption key is enabled.   |
| `openpages.encryption-keystore.get` | An event is generated when a encryption key retrieve. |
{: caption="Actions that generate encryption keystore events (UI)" caption-side="bottom"}

Environment migration:

| Action:                                   | Description:                                                                          |
| ----------------------------------------- | ------------------------------------------------------------------------------------- |
| `openpages.configuration-export.list` |  |
| `openpages.configuration.get` | An event is generated when a configuration export/import item is fetched. |
| `openpages.configuration-export.start` | An event is generated when an import is started in the Import Configuration UI. |
| `openpages.configuration-validation.start` |  |
| `openpages.configuration-import.start` | An event is generated when an import is started in the Import Configuration UI. |
| `openpages.configuration-import.list` | An event is generated when configuration import history is listed in the UI. |
{: caption="Actions that generate environment migration events (UI)" caption-side="bottom"}

Localization \(object text and application text\):

| Action:                               | Description:                                                                    |
| ------------------------------------- | ------------------------------------------------------------------------------- |
| `openpages.object-text-key.list` | An event is generated when a list of object text key strings is fetched. |
| `openpages.application-text.update` | An event is generated when an application text string is updated. |
| `openpages.application-text-key.list` | An event is generated when a list of user-defined application text keys is fetched. |
| `openpages.object-text.update` | An event is generated when an object text string is updated. |
| `openpages.object-text.list` | An event is generated when a list of object text strings is fetched. |
{: caption="Actions that generate object text and application text localization events (UI)" caption-side="bottom"}

Logs, processes, trace logs:

| Action:                               | Description:                                                                       |
| ------------------------------------- | ---------------------------------------------------------------------------------- |
| `openpages.log-collector-logs.download` | An event is generated when Log Collector log .zip file is downloaded. |
| `openpages.process-log.list` | An event is generated when a list of background process logs is fetched. |
| `openpages.addFieldGroupProcess.satrt` | An event is generated when a field group operation is started. |
| `openpages.log-collector.start` | An event is generated when Log Collector is started. |
| `openpages.log-collector-logs.delete` | An event is generated when a Log Collector log file is deleted from the **Other > Logs** UI. |
| `openpages.trace-options.list` | An event is generated when a list of trace options is fetched. |
| `openpages.program.start` | An event is generated when questionnaire program is launched. |
| `openpages.process.get` | An event is generated when a background process is fetched. |
| `openpages.trace-options.update` | An event is generated when the trace logging settings are updated in the **Other > Logs > System tracing options** UI. |
| `openpages.process.list` | An event is generated when a background process list is fetched. |
{: caption="Actions that generate object text and application text localization events (UI)" caption-side="bottom"}

Role templates:

| Action:                                 | Description:                                                                    |
| --------------------------------------- | ------------------------------------------------------------------------------- |
| `openpages.role-template-access.delete` | An event is generated when an object type is removed from a role template. |
| `openpages.role-template-access.update` | An event is generated when the access controls for object type are changed for a role template. |
| `openpages.role-template.list` | An event is generated when a role template list is fetched. |
| `openpages.role.set` | An event is generated when roles are assigned to users or groups. |
| `openpages.role-template.enable` | An event is generated when a role template is enabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the role template is enabled. |
| `openpages.role-template.update` | An event is generated when the properties of a role template, such as its Name and Description, are updated. |
| `openpages.role-template.disable` | An event is generated when a role template is disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `true` and `newValue` is set to `false`, the role template is disabled. |
| `openpages.role.revoke` | An event is generated when a role template is removed from a user or group. |
| `openpages.role-template-lock.set-on` | An event is generated when a role template is locked. |
| `openpages.role-template.create` | An event is generated when a role template is created. |
| `openpages.role-template-app-permission.update` | An event is generated when the application permissions that are assigned to a role template are changed. |
| `openpages.role-template.delete` | An event is generated when a role template is deleted. |
| `openpages.role-template-access.add` | An event is generated when an object type is added to a role template. |
| `openpages.role-template.get` | An event is generated when a role template is fetched. |
| `openpages.role-template-lock.set-off` | An event is generated when a role template is unlocked. |
{: caption="Actions that generate role template events (UI)" caption-side="bottom"}

Security rules:

| Action:                                         | Description:                                                                                 |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `openpages.field-level-security-rule.delete` | An event is generated when a field-level security rule is deleted. |
| `openpages.security-rule.get` | An event is generated when a list of security rules across object types is fetched. |
| `openpages.field-level-security-rule.update` | An event is generated when a field-level security rule is modified. |
| `openpages.record-level-security-rule.enable` | An event is generated when a record-level security rule is enabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the record-level security rule is enabled. |
| `openpages.security-rule.list` | An event is generated when a list of security rules across object types is fetched. |
| `openpages.field-level-security-rule.enable` | An event is generated when a field-level security rule is enabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the field-level security rule is enabled. |
| `openpages.field-level-security-rule.validate` | An event is generated when a field-level security rule is validated. |
| `openpages.record-level-security-rule.validate` | An event is generated when a record-level security rule is validated. |
| `openpages.record-level-security-rule.update` | An event is generated when a record-level security rule is modified. |
| `openpages.record-level-security-rule.delete` | An event is generated when a record-level security rule is deleted. |
| `openpages.field-level-security-rule.create` | An event is generated when a field-level security rule is created. |
| `openpages.record-level-security-rule.create` | An event is generated when a record-level security rule is created. |
{: caption="Actions that generate security rule events (UI)" caption-side="bottom"}

Settings:

| Action:                      | Description:                                                                |
| ---------------------------- | --------------------------------------------------------------------------- |
| `openpages.setting-folder.add` | An event is generated when a setting folder is created. |
| `openpages.setting.create` | An event is generated when a setting is created. |
| `openpages.setting.delete` | An event is generated when a setting is deleted. |
| `openpages.setting.get` | An event is generated when a setting is fetched. |
| `openpages.report.evaluate` |  |
| `openpages.setting.list` | An event is generated when a list of settings is fetched. |
| `openpages.setting.copy` | An event is generated when a setting is copied. |
| `openpages.setting.update` | An event is generated when the value of a setting is modified. |
{: caption="Actions that generate settings events (UI)" caption-side="bottom"}

System admin mode:

| Action:                               | Description:                                              |
| ------------------------------------- | --------------------------------------------------------- |
| `openpages.system-admin-mode.disable` | An event is generated when System Admin Mode is disabled. |
| `openpages.system-admin-mode.enable` | An event is generated when System Admin Mode is enabled. |
{: caption="Actions that generate system admin mode events (UI)" caption-side="bottom"}

System files:

| Action:                                      | Description:                                                              |
| -------------------------------------------- | ------------------------------------------------------------------------- |
| `openpages.system-file-resource-access.update` | An event is generated when access to the system file resource is updated. |
| `openpages.system-file-resource.list` | An event is generated when a system file resource list is fetched. |
| `openpages.system-file-resource.get` | An event is generated when a system file resource is fetched. |
| `openpages.system-file-resource.create` | An event is generated when a system file resource is added. |
| `openpages.system-file-resource.delete` | An event is generated when system file resource is deleted. |
| `openpages.system-file-resource-move.commit` | An event is generated when a system file resource is moved. |
| `openpages.system-file-resource-copy.commit` | An event is generated when a system file resource is copied. |
| `openpages.page-and-template.list` | An event is generated when a list of pages and templates is fetched. |
| `openpages.system-file-resource-access.delete` | An event is generated when a system file resource is deleted. |
| `openpages.system-file-resource-rename.commit` | An event is generated when a system file resource is renamed. |
| `openpages.system-file-resource-access.list` | An event is generated when a list of accesses to the system file resource is fetched. |
| `openpages.system-file-resource.update` | An event is generated when a system file resource is modified. |
{: caption="Actions that generate system files events (UI)" caption-side="bottom"}


## Object types, profiles, schema, object instances events
{: #object-types}

Field dependencies:

| Action:                           | Description:                                               |
| --------------------------------- | ---------------------------------------------------------- |
| `openpages.field-dependency.delete` | An event is generated when a field dependency is deleted. |
| `openpages.field-dependency.update` | An event is generated when a field dependency is modified. |
| `openpages.field-dependency.disable` | An event is generated when a field dependency is disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `true` and `newValue` is set to `false`, the field dependency is disabled. |
| `openpages.field-dependency.enable` | An event is generated when a field dependency is enabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the field dependency is enabled. |
| `openpages.field-dependency.create` | An event is generated when a field dependency is created. |
| `openpages.field-dependency.list` | An event is generated when a list of field dependencies is fetched. |
{: caption="Actions that generate field dependency events (UI)" caption-side="bottom"}

Field groups, fields, and schema:

| Action:                         | Description:                                                              |
| ------------------------------- | ------------------------------------------------------------------------- |
| `openpages.field-groups.remove` | An event is generated when a field group is removed from an object type. |
| `openpages.field-groups.add` | An event is generated when a field group is added to an object type. |
| `openpages.solution.get` | An event is generated when a solution is fetched. |
| `openpages.object-type.update` | An event is generated when the properties of an object type are modified. |
| `openpages.field.update` | An event is generated when a field is modified. |
| `openpages.field-group.list` | An event is generated when a list of field groups is fetched. |
| `openpages.field-groups.delete` | An event is generated when a field group is deleted. |
| `openpages.solution-profile.list` | An event is generated when object types with profiles are fetched. |
| `openpages.field-groups.update` | An event is generated when a field group is updated. |
| `openpages.field.list` | An event is generated when a list of fields is fetched. |
| `openpages.system-fields-names.list` | An event is generated when a list of system fields for an object type is fetched. |
| `openpages.object-type-tag.enable` | An event is generated when a tag is enabled or disabled. |
| `openpages.filters.list` | An event is generated when a list of object filters is fetched. |
| `openpages.field.create` | An event is generated when a field is created. |
| `openpages.object-type.list` | An event is generated when a list of object types is fetched. |
| `openpages.field-groups.create` | An event is generated when a field group is created. |
{: caption="Actions that generate field, field group, and schema events (UI)" caption-side="bottom"}

Filters:

| Action:                        | Description:                                                              |
| ------------------------------ | ------------------------------------------------------------------------- |
| `openpages.object-filter.get` | An event is generated when an object filter is fetched. |
| `openpages.object-filter.delete` | An event is generated when a public filter is deleted. |
| `openpages.object-filter-fields.list` | An event is generated when a list of object filter fields is fetched. |
| `openpages.object-filter.create` | An event is generated when a public filter is defined for an object type. |
| `openpages.object-filter.list` | An event is generated when a list of object filters is fetched. |
{: caption="Actions that generate filter events (UI)" caption-side="bottom"}

Profiles:

| Action:                                | Description:                                                                  |
| -------------------------------------- | ----------------------------------------------------------------------------- |
| `openpages.profile.delete` | An event is generated when a profile is deleted. |
| `openpages.profile-object-filter.add` | An event is generated when a public filter is added to a profile. |
| `openpages.profile-report.enable` | An event is generated when reports are enabled or disabled on a profile. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, reports are enabled on the profile. When `initialValue` is set to `true` and `newValue` is set to `false`, reports are disabled on the profile. |
| `openpages.profile-actor.remove` | An event is generated when users or groups are removed from a profile. |
| `openpages.profile.list` | An event is generated when a list of object profiles is fetched. |
| `openpages.profile-object-type.get` | An event is generated when an object type for a profile is fetched. |
| `openpages.profile.get` | An event is generated when an object profile is fetched. |
| `openpages.profile-object-filter.delete` | An event is generated when a public filter is removed from a profile. |
| `openpages.profile-object-field.delete` | An event is generated when an object field is removed from a profile. |
| `openpages.profile-object-field.update` | An event is generated when an object field is modified on a profile. |
| `openpages.profile-report.disable` | An event is generated when reports are enabled or disabled on a profile. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, reports are enabled on the profile. When `initialValue` is set to `true` and `newValue` is set to `false`, reports are disabled on the profile. |
| `openpages.profile.enable` | An event is generated when a profile is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the profile is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the profile is disabled. |
| `openpages.profile-actor.list` | An event is generated when a list of users or groups associated to a profile is fetched. |
| `openpages.profile-object-field.add` | An event is generated when an object field is added to a profile. |
| `openpages.profile.disable` | An event is generated when a profile is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the profile is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the profile is disabled. |
| `openpages.profile-object-type.add` | An event is generated when an object type is added to a profile. |
| `openpages.profile-report.delete` | An event is generated when reports are deleted from a profile. |
| `openpages.profile.create` | An event is generated when a profile is created. |
| `openpages.profile-object-type.list` | An event is generated when a list of object types for a profile is fetched. |
| `openpages.profile-object-field.list` | An event is generated when a list of object fields for a profile is fetched. |
| `openpages.profile-object-type.delete` | An event is generated when an object type is removed from a profile |
| `openpages.profile.update` | An event is generated when a profile is modified. |
| `openpages.profile-report.add` | An event is generated when reports are added to a profile. |
| `openpages.profile-actor.add` | An event is generated when users or groups are added to a profile. |
| `openpages.fallback-profile.get` |  |
{: caption="Actions that generate profile events (UI)" caption-side="bottom"}

Objects:

| Action:                              | Description:                                                                  |
| ------------------------------------ | ----------------------------------------------------------------------------- |
| `openpages.resource.get` | An event is generated when an object instance is fetched to a task view. |
| `openpages.resource.create` | An event is generated when an object instance is created. |
| `openpages.resource.update` | An event is generated when an object instance is modified. |
| `openpages.resource-lock.set-off` | An event is generated when an object instance is unlocked. |
| `openpages.resource-list.update` | An event is generated when object instances are updated by a bulk operation. |
| `openpages.resource-lock.set-on` | An event is generated when an object instance is locked. |
| `openpages.file-resource.create` | An event is generated when an attachment is created. |
| `openpages.resource-move.commit` | An event is generated when an object instance is moved. |
| `openpages.file-resource-version.list` | An event is generated when a list of attachment versions is fetched. |
| `openpages.resource.export` | An event is generated when a list of object instances is exported. |
| `openpages.resource.delete` | An event is generated when an object instance is deleted. |
| `openpages.resource.list` | An event is generated when a list of object instances is fetched. |
| `openpages.file-resource.update` | An event is generated when an attachment is modified. |
{: caption="Actions that generate object events (UI)" caption-side="bottom"}

Object resets:

| Action:                      | Description:                                                              |
| ---------------------------- | ------------------------------------------------------------------------- |
| `openpages.object-reset-logs.get` |  |
| `openpages.object-reset.get` | An event is generated when the result of an object-reset operation is fetched. |
{: caption="Actions that generate object reset events (UI)" caption-side="bottom"}


Object type associations:

| Action:                                    | Description:                                                                   |
| ------------------------------------------ | ------------------------------------------------------------------------------ |
| `openpages.object-relationship.update` | An event is generated when an object instance relationship is updated. |
| `openpages.resource-copy.commit` | An event is generated when object instances are copied recursively. |
| `openpages.object-relationship.list` | An event is generated when a list of object type relationships is fetched. |
| `openpages.object-relationship.enable` | An event is generated when an object type relationship is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the object type relationship is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the object type relationship is disabled. |
| `openpages.resource-primary-parent.set` | An event is generated when primary parent is reassigned for an object instance. |
| `openpages.object-relationship.disable` | An event is generated when an object type relationship is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the object type relationship is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the object type relationship is disabled. |
| `openpages.resource.remove` | An event is generated when an object instance relationship is removed. |
| `openpages.resource-list.remove` | An event is generated when a list of object instance relationships is removed. |
| `openpages.resource.add` | An event is generated when an object instance relationship is added. |
{: caption="Actions that generate object type associations events (UI)" caption-side="bottom"}

Recursive object types:

| Action:                                 | Description:                                                       |
| --------------------------------------- | ------------------------------------------------------------------ |
| `openpages.recursive-object-level.create` | An event is generated when a recursive object level is created. |
| `openpages.recursive-object-level.list` | An event is generated when recursive object level list is fetched. |
| `openpages.recursive-object-level.delete` | An event is generated when a recursive object level is deleted. |
{: caption="Actions that generate recursive object type events (UI)" caption-side="bottom"}

Solutions:

| Action:                          | Description:                                                  |
| -------------------------------- | ------------------------------------------------------------- |
| `openpages.field-exclusion.update` | An event is generated when a field exclusion is updated. |
| `openpages.field-exclusion.delete` | An event is generated when a field exclusion is deleted. |
| `openpages.solution.create` | An event is generated when a solution is created. |
| `openpages.field-exclusion.create` | An event is generated when a field exclusion is created. |
| `openpages.solution.delete` | An event is generated when a solution is deleted. |
| `openpages.solution.get` | An event is generated when a solution is fetched. |
| `openpages.solution.list` | An event is generated when a list of solutions is fetched. |
| `openpages.field-exclusion.list` | An event is generated when a list of field exclusions is fetched. |
| `openpages.solution.update` | An event is generated when a solution is updated. |
{: caption="Actions that generate solution events (UI)" caption-side="bottom"}

## Calculations, workflows, views, and other user interface events
{: #calc-workflow}

Calculations:

| Action:                               | Description:                                                          |
| ------------------------------------- | --------------------------------------------------------------------- |
| `openpages.calculation-draft.publish` | An event is generated when a calculation is published. |
| `openpages.calculation-draft.clear` | An event is generated when a draft calculation is discarded. |
| `openpages.bulk-calculation.start` | An event is generated when a calculation is run for object instances. |
| `openpages.calculation.disable` |  An event is generated when a calculation is disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `true` and `newValue` is set to `false`, the calculation is disabled.  |
| `openpages.calculation.enable` | An event is generated when a calculation is enabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the calculation is enabled.  |
| `openpages.calculation.update` | An event is generated when a calculation is updated. |
| `openpages.calculation.list` | An event is generated when a list of calculations is fetched. |
| `openpages.calculation.get` | An event is generated when a calculation is fetched. |
| `openpages.calculation.delete` | An event is generated when a calculation is deleted. |
| `openpages.calculation.create` | An event is generated when a calculation is created. |
{: caption="Actions that generate calculation events (UI)" caption-side="bottom"}

Dashboards:

| Action:                                   | Description:                                                                   |
| ----------------------------------------- | ------------------------------------------------------------------------------ |
| `openpages.admin-dashboard.update` | An event is generated when an administrative dashboard is updated. |
| `openpages.admin-dashboard.list` | An event is generated when a list of administrative dashboards is fetched. |
| `openpages.admin-dashboard.get` | An event is generated when an administrative dashboard is fetched. |
| `openpages.admin-dashboard.create` | An event is generated when an administrative dashboard is created. |
| `openpages.admin-dashboard.enable` | An event is generated when an administrative dashboard is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the administration dashboard is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the administration dashboard is disabled. |
| `openpages.user-dashboard.update` | An event is generated when a user dashboard is updated. |
| `openpages.admin-dashboard-draft.clear` | An event is generated when an administrative dashboard draft is discarded. |
| `openpages.admin-dashboard.disable` | An event is generated when an administrative dashboard is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the administration dashboard is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the administration dashboard is disabled. |
| `openpages.user-dashboard.get` | An event is generated when a user dashboard is loaded. |
| `openpages.admin-dashboard-draft.publish` | An event is generated when an administrative dashboard is published. |
| `openpages.admin-dashboard.delete` | An event is generated when an administrative dashboard is deleted. |
{: caption="Actions that generate dashboard events (UI)" caption-side="bottom"}

FastMap:

| Action:                    | Description:                                                       |
| -------------------------- | ------------------------------------------------------------------ |
| `openpages.fastmap.validate` | An event is generated when a FastMap validation is started. |
| `openpages.fastmap.import` | An event is generated when a FastMap import is started. |
{: caption="Actions that generate FastMap events (UI)" caption-side="bottom"}

File attachments:

| Action:                                   | Description:                                                    |
| ----------------------------------------- | --------------------------------------------------------------- |
| `openpages.file-type-search.enable` | An event is generated when global search is enabled or disabled for an attachment file type. |
| `openpages.file-type.disable` | An event is generated when an attachment file type is disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
| `openpages.file-type.create` | An event is generated when an attachment file type is created. |
| `openpages.file-resource-checkout.clear` | An event is generated when an attachment check-out is canceled. |
| `openpages.file-resource-checkout.set-on` | An event is generated when an attachment is checked out. |
| `openpages.file-resource.download` | An event is generated when a file is downloaded. |
| `openpages.file-type.enable` | An event is generated when an attachment file type is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the attachment file type is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the attachment file type is disabled. |
| `openpages.file-resource-checkout.commit` | An event is generated when an attachment is checked in. |
{: caption="Actions that generate file attachment events (UI)" caption-side="bottom"}

Folders:

| Action:                          | Description:                                    |
| -------------------------------- | ----------------------------------------------- |
| `openpages.folder.create` | An event is generated when a folder is created. |
| `openpages.folder.delete` | An event is generated when a folder is deleted. |
{: caption="Actions that generate folder events (UI)" caption-side="bottom"}


Questionnaires:

| Action:                                              | Description:                                                                                            |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `openpages.questionnaire-logic.evaluate` | An event is generated when questionnaire advanced logic is evaluated. |
| `openpages.questionnaire-attachement.import` | An event is generated when an attachment is added to a questionnaire. |
| `openpages.questionnaire-template.copy` | An event is generated when a questionnaire template is copied. |
| `openpages.questionnaire-template-reorder.commit` | An event is generated when questions are reordered in a questionnaire template. |
| `openpages.questionnaire-template-answers.copy` | An event is generated when question answers are copied. |
| `openpages.questionnaire-template.update` | An event is generated when a questionnaire template is updated. |
| `openpages.questionnaire-template.get` | An event is generated when a questionnaire template is fetched. |
| `openpages.questionnaire.get` | An event is generated when a questionnaire assessment is fetched. |
| `openpages.questionnaire-template-default-object.add` | An event is generated when default objects are added a questionnaire template. |
{: caption="Actions that generate questionnaire events (UI)" caption-side="bottom"}

Rules \(Regulatory Event rules\):

| Action:               | Description:                                                                    |
| --------------------- | ------------------------------------------------------------------------------- |
| `openpages.rule.delete` | An event is generated when a rule in the Regulatory Event Rules UI is deleted. |
| `openpages.rule.create` | An event is generated when a rule is created in the Regulatory Event Rules UI. |
| `openpages.rule.get` | An event is generated when a regulatory event rule is fetched. |
| `openpages.rule.list` | An event is generated when rules in the Regulatory Event Rules UI is fetched. |
| `openpages.rule.update` | An event is generated when a rule in the Regulatory Event Rules UI is modified. |
| `openpages.rule-supported-types.list` | An event is generated when a list of supported object types of rules is fetched. |
| `openpages.rule.enable` | An event is generated when a rule in the Regulatory Event Rules UI is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the rule in the Regulatory Event Rules UI is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the rule in the Regulatory Event Rules UI is disabled. |
| `openpages.rule.disable` | An event is generated when a rule in the Regulatory Event Rules UI is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the rule in the Regulatory Event Rules UI is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the rule in the Regulatory Event Rules UI is disabled. |
{: caption="Actions that generate rule events in the Regulatory Event Rules (UI)" caption-side="bottom"}

Scheduler jobs:

| Action:                          | Description:                                                       |
| -------------------------------- | ------------------------------------------------------------------ |
| `openpages.scheduler-job.delete` | An event is generated when a scheduler job is deleted. |
| `openpages.scheduler-job.get` | An event is generated when a scheduler job is fetched. |
| `openpages.scheduler-job.create` | An event is generated when scheduler job is created. |
| `openpages.scheduler-job.disable` | An event is generated when a scheduler job is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the scheduler job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the scheduler job is disabled. |
| `openpages.scheduler-job.enable` | An event is generated when a scheduler job is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the scheduler job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the scheduler job is disabled. |
| `openpages.scheduler-job.start` | An event is generated when a scheduler job is started |
| `openpages.scheduler-job.update` | An event is generated when scheduler job is updated. |
| `openpages.scheduler-job.list` |  |
| `openpages.scheduler-job-log.list` | An event is generated when a job execution log is viewed. |
{: caption="Actions that generate schedular job events (UI)" caption-side="bottom"}

Tags:

| Action:                          | Description:                                                     |
| -------------------------------- | ---------------------------------------------------------------- |
| `openpages.tag-association.delete` | An event is generated when tags for a resource are deleted. |
| `openpages.tag-association.get` | An event is generated when tags for a resource are fetched. |
| `openpages.tag.enable` | An event is generated when a tag is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the tag job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the tag is disabled. |
| `openpages.tag.list` | An event is generated when a list of tags is fetched. |
| `openpages.tag-association.update` | An event is generated when tags for a resource are updated. |
| `openpages.tag.update` | An event is generated when the properties of a tag are modified. |
| `openpages.tag.create` | An event is generated when a tag is created. |
| `openpages.tag-association.add` | An event is generated when tags for a resource are added. |
| `openpages.tag-association.create` | An event is generated when a tag is added object instance. |
{: caption="Actions that generate tag events (UI)" caption-side="bottom"}

Themes:

| Action:                | Description:                                               |
| ---------------------- | ---------------------------------------------------------- |
| `openpages.theme.delete` | An event is generated when a theme is deleted. |
| `openpages.theme.create` | An event is generated when a theme is created. |
| `openpages.theme.list` | An event is generated when a list of themes is fetched. |
| `openpages.theme.disable` | An event is generated when a theme is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the theme job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the theme is disabled.  |
| `openpages.theme.update` | An event is generated when a theme is updated. |
| `openpages.theme.get` | An event is generated when a theme is fetched. |
| `openpages.theme.enable` | An event is generated when a theme is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the theme job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the theme is disabled.  |
{: caption="Actions that generate theme events (UI)" caption-side="bottom"}

Workflows:

| Action:                                     | Description:                                                                |
| ------------------------------------------- | --------------------------------------------------------------------------- |
| `openpages.workflow-draft.publish` | An event is generated when a workflow definition is published. |
| `openpages.resource-workflow.start` | An event is generated when a workflow is started. |
| `openpages.workflow.create` | An event is generated when a workflow definition is created. |
| `openpages.workflow-draft.clear` | An event is generated when a draft of workflow definition is discarded. |
| `openpages.resource.get` | An event is generated when an object instance is fetched to a task view. |
| `openpages.workflow.disable` | An event is generated when a workflow definition is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the workflow definition job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the workflow definition is disabled.  |
| `openpages.workflow-resource-synchronization.evaluate` | An event is generated when a workflow is synchronized. |
| `openpages.workflow.enable` | An event is generated when a workflow definition is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the workflow definition job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the workflow definition is disabled.  |
| `openpages.workflow-resource-list-action.start` | An event is generated when workflow action is processed in bulk. |
| `openpages.workflow-resource.list` | An event is generated when a list of workflows is fetched.         |
| `openpages.workflow.delete` | An event is generated when a workflow definition is deleted. |
| `openpages.workflow-resource-list.start` | An event is generated when workflows are started for a workflow definition. |
| `openpages.workflow-resource-action.validate` | An event is generated when Watson™ Translator configuration is validated. |
| `openpages.workflow.list` | An event is generated when a draft of a workflow definition is discarded. |
| `openpages.workflow.update` | An event is generated when a workflow definition is updated. |
| `openpages.workflow.get` | An event is generated when a workflow definition is fetched. |
| `openpages.workflow-resource.stop` | An event is generated when workflows are stopped. |
| `openpages.resource-workflow-action.start` | An event is generated when a workflow action is processed. |
{: caption="Actions that generate workflow events (UI)" caption-side="bottom"}

Views:

| Action:                      | Description:                                                    |
| ---------------------------- | --------------------------------------------------------------- |
| `openpages.view.disable` | An event is generated when a view is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the view job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the view is disabled.     |
| `openpages.view.list` | An event is generated when a list of views is fetched. |
| `openpages.view-draft.clear` | An event is generated when the changes to a view are discarded. |
| `openpages.view.create` | An event is generated when a view is created. |
| `openpages.view.get` | An event is generated when a view is fetched. |
| `openpages.admin-view.create` | An event is generated when an Admin View is created. |
| `openpages.view.validate` | An event is generated when a view is validated. |
| `openpages.view.delete` | An event is generated when a view is deleted. |
| `openpages.view.update` | An event is generated when a view is modified. |
| `openpages.view.enable` | An event is generated when a view is enabled or disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the view job is enabled. When `initialValue` is set to `true` and `newValue` is set to `false`, the view is disabled.     |
| `openpages.view-draft.publish` | An event is generated when a view is published. |
{: caption="Actions that generate view events (UI)" caption-side="bottom"}


## Integration-related events
{: #integrations}

AI models:

| Action:                                     | Description:                                                       |
| ------------------------------------------- | ------------------------------------------------------------------ |
| `openpages.ai-model-configuration.validate` | An event is generated when an AI model configuration is validated. |
| `openpages.ai-model-configuration.update` | An event is generated when an AI model configuration is updated. |
| `openpages.ai-model-configuration.delete` | An event is generated when an AI model configuration is deleted. |
| `openpages.ai-model-configuration.create` | An event is generated when an AI model configuration is created. |
| `openpages.ai-model-suggestion.evaluate` | An event is generated when an AI model suggests an insight. |
| `openpages.ai-model-configuration.get` | An event is generated when an AI model configurations is fetched. |
| `openpages.ai-model-configuration.list` | An event is generated when AI model configurations are listed. |
{: caption="Actions that generate AI model events (UI)" caption-side="bottom"}


Classifiers:

| Action:                              | Description:                                                 |
| ------------------------------------ | ------------------------------------------------------------ |
| `openpages.watson-classifier.delete` | An event is generated when a Watson™ classifier is deleted. |
| `openpages.watson-classifier.validate` | An event is generated when a Watson™ classifier is validated. |
| `openpages.watson-classifier.update` | An event is generated when a Watson™ classifier is updated. |
| `openpages.watson-classifier.create` | An event is generated when a Watson™ classifier is created. |
{: caption="Actions that generate watson classifier events (UI)" caption-side="bottom"}

Microsoft Office:

| Action:                          | Description:                                                                 |
| -------------------------------- | ---------------------------------------------------------------------------- |
| `openpages.msoffice-resource.commit` | An event is generated when a Microsoft™ Office file is saved. |
| `openpages.msoffice-resource.edit` | An event is generated when a Microsoft™ Office file editing session is started. |
{: caption="Actions that generate Microsoft Office events (UI)" caption-side="bottom"}

watsonx Assistant:

| Action:                              | Description:                                                              |
| ------------------------------------ | ------------------------------------------------------------------------- |
| `openpages.watson-assistant.validate` | An event is generated when  an IBM watsonx™ Assistant  configuration is validated. |
| `openpages.watson-assistant.get` | An event is generated when an IBM watsonx™ Assistant configuration is fetched. |
| `openpages.watson-assistant.configure` | An event is generated when an IBM watsonx™ Assistant  is configured. |
{: caption="Actions that generate watsonx Assistant events (UI)" caption-side="bottom"}


## Feed provider events
{: #feeds}

Reg-Track:

| Action:                    | Description:                                                          |
| -------------------------- | --------------------------------------------------------------------- |
| `openpages.reg-track.get` | An event is generated when a reg-track feed configuration is fetched. |
| `openpages.reg-track.update` | An event is generated when a reg-track feed configuration is updated. |
| `openpages.reg-track.import` | An event is generated when a reg-track feed is imported. |
{: caption="Actions that generate reg-track feed events (UI)" caption-side="bottom"}

Thomson Reuters:

| Action:                             | Description:                                                                    |
| ----------------------------------- | ------------------------------------------------------------------------------- |
| `openpages.trri.import` | An event is generated when Thomson Reuters feed is imported. |
| `openpages.taxonomy-mapping.upload` | An event is generated when Thomson Reuters feed taxonomy mapping is uploaded. |
| `openpages.trri.get` | An event is generated when Thomson Reuters feed configuration is fetched. |
| `openpages.taxonomy-mapping.download` | An event is generated when Thomson Reuters feed taxonomy mapping is downloaded. |
| `openpages.trri.update` | An event is generated when Thomson Reuters feed configuration is updated. |
{: caption="Actions that generate Thomson Reuters feed events (UI)" caption-side="bottom"}

Wolters Kluwer:

| Action:             | Description:                                                             |
| ------------------- | ------------------------------------------------------------------------ |
| `openpages.wk.get` | An event is generated when Wolters Kluwer feed configuration is fetched. |
| `openpages.wk.update` | An event is generated when Wolters Kluwer feed configuration is updated. |
| `openpages.wk.import` | An event is generated when Wolters Kluwer feed is imported. |
{: caption="Actions that generate Wolters Kluwer feed events (UI)" caption-side="bottom"}

## API events
{: #api-events}

| Action:                                         | Description:                                                                             |
| ----------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `openpages.group-role-assignment.delete` | An event is generated when a role is removed from a group. |
| `openpages.folder.update` | An event is generated when a folder is updated. |
| `openpages.object-manager.load` | An event is generated when object-manager load has started. |
| `openpages.tag.get` | An event is generated when a tag is fetched. |
| `openpages.workflow-resource.get` | An event is generated when a workflow is fetched. |
| `openpages.process.get` | An event is generated when a background process is fetched. |
| `openpages.object-manager.dump` | An event is generated when object-manager dump has started. |
| `openpages.user-role-assignment.add` | An event is generated when a role is assigned to a user. |
| `openpages.folder.get` | An event is generated when a folder is fetched. |
| `openpages.root-folder.get` | An event is generated when root folders of object types are fetched. |
| `openpages.scim-service-provider-configuration.get` | An event is generated when SCIM service provider configuration is fetched. |
| `openpages.tag.create` | An event is generated when a tag is created. |
| `openpages.tag-association.add` | An event is generated when tags for a resource are added. |
| `openpages.object-type.list` | An event is generated when a list of object types is fetched. |
| `openpages.user.list` | An event is generated when a list of users is fetched. |
| `openpages.currency.enable` | An event is generated when a currency is enabled. Under the `requestData.update` JSON field, when `initialValue` is set to `false` and `newValue` is set to `true`, the currency is enabled. |
| `openpages.sub-group.add` | An event is generated when a group member is added to a group. |
| `openpages.role-template-app-permission.list` | An event is generated when a list of application permissions for a role template are fetched. |
| `openpages.base-currency.list` | An event is generated when base currencies are listed. |
| `openpages.group.update` | An event is generated when a group is updated. |
| `openpages.app-permission.get` | An event is generated when an application permission is fetched. |
| `openpages.currency.update` | An event is generated when a currency is updated. |
| `openpages.folder.create` | An event is generated when a folder is created. |
| `openpages.scim-schema.list` | An event is generated when a list of SCIM schemas is fetched. |
| `openpages.folder-template.get` | An event is generated when a folder template is fetched. |
| `openpages.resource.create` | An event is generated when an object instance is created. |
| `openpages.resource-association.delete` | An event is generated when an object instance is dissociated from a parent or a child. |
| `openpages.currency.list` | An event is generated when a list of currencies are fetched. |
| `openpages.trace-options.update` | An event is generated when the trace logging settings are updated in the **Other > Logs > System tracing options** UI. |
| `openpages.user.update` | An event is generated when a user  is modified. |
| `openpages.bulkRequest.bulk processing` |  |
| `openpages.user-anonimization.set` | An event is generated when user attributes are changed to remove private information that could be used to identify a user. |
| `openpages.object-type-unclaimed.get` | An event is generated when a list of unentitled object types is fetched. |
| `openpages.resource-copy.commit` | An event is generated when an object instances are copied recursively. |
| `openpages.setting.get` | An event is generated when a setting is fetched. |
| `openpages.sub-group.list` | An event is generated when a list of subgroup members is fetched. |
| `openpages.workflow.list` | An event is generated when a list of workflow definitions is fetched. |
| `openpages.scim-resource-type.get` | An event is generated when an SCIM resource type is fetched. |
| `openpages.tag-association.delete` | An event is generated when tags for a resource is deleted. |
| `openpages.workflow-resource-action.commit` | An event is generated when a workflow action is submitted. |
| `openpages.resource-lock.set-off` | An event is generated when an object instance is unlocked. |
| `openpages.group-permission.list` | An event is generated when a list of group permissions is fetched.  |
| `openpages.process.stop` | An event is generated when a long running process is stopped. |
| `openpages.tag.update` | An event is generated when the properties of a tag are modified. |
| `openpages.file-resource.download` | An event is generated when a file is downloaded. |
| `openpages.resource-move.commit` | An event is generated when an object instance is moved. |
| `openpages.group-member.list` | An event is generated when a list of group members is fetched. |
| `openpages.resource-association.list` | An event is generated when a list of object instance associations  is fetched. |
| `openpages.currency-history.list` | An event is generated when a currency update history is listed. |
| `openpages.role-template-access.list` | An event is generated when a list of accesses to a role template is fetched. |
| `openpages.resource-association.get` | An event is generated when an object instance association is fetched. |
| `openpages.resource-template.get` | An event is generated when an empty object instance template is fetched. |
| `openpages.object-type.get` | An event is generated when an object type is fetched. |
| `openpages.user.get` | An event is generated when a user is fetched. |
| `openpages.folder-permission.get` | An event is generated when folder permissions are fetched. |
| `openpages.profile-object-field.list` | An event is generated when a list of object fields for a profile is fetched. |
| `openpages.workflow-resource.search` | An event is generated when workflows are searched. |
| `openpages.sub-group.delete` | An event is generated when a group member is removed from a group. |
| `openpages.group.get` | An event is generated when a group is fetched. |
| `openpages.tag-association.list` | An event is generated when a list of associated tags for an object instance is fetched. |
| `openpages.folder.delete` | An event is generated when a folder is deleted. |
| `openpages.group-member.add` | An event is generated when a user is added to a group. |
| `openpages.file-resource.upload` | An event is generated when a file is uploaded. |
| `openpages.group-member.delete` | An event is generated when a user is removed from a group. |
| `openpages.resource-activity.list` | An event is generated when a list of changes to an object is displayed on the Activity tab. |
| `openpages.user-password.reset` | An event is generated when a user password is reset. |
| `openpages.role-template.get` | An event is generated when a role template is fetched. |
| `openpages.setting.list` | An event is generated when a list of settings is fetched. |
| `openpages.currency.disable` | An event is generated when a currency is disabled. Under the `requestData.update` JSON field, when `initialValue` is set to `true` and `newValue` is set to `false`, the currency is disabled. |
| `openpages.group.list` | An event is generated when a list of groups is fetched. |
| `openpages.profile.list` | An event is generated when a list of object profiles is fetched. |
| `openpages.user-membership.list` | An event is generated when a list of user group memberships is fetched. |
| `openpages.object-type-association.list` | An event is generated when a list of object type associations is fetched. |
| `openpages.scim-resource-type.list` | An event is generated when an SCIM resource type is fetched. |
| `openpages.resource.query` | An event is generated when object instances are queried. |
| `openpages.resource.get` | An event is generated when an object instance is fetched to a task view. |
| `openpages.system-admin-mode.get` | An event is generated when the System Admin Mode flag is fetched. |
| `openpages.system-admin-mode.disable` | An event is generated when System Admin Mode is disabled. |
| `openpages.group.create` | An event is generated when a group is created. |
| `openpages.workflow-version.get` | An event is generated when a workflow definition version is fetched. |
| `openpages.system-admin-mode.enable` | An event is generated when System Admin Mode is enabled. |
| `openpages.group-role-assignment.list` | An event is generated when a list of role assignments for a group is fetched. |
| `openpages.resource.delete` | An event is generated when an object instance is deleted. |
| `openpages.application-text.list` | An event is generated when an application text string list is fetched. |
| `openpages.currency-list.update` | An event is generated when currency exchnage rates are updated in bulk. |
| `openpages.currency.get` | An event is generated when a currency is fetched. |
| `openpages.group-role-assignment.add` | An event is generated when a role is assigned to a group. |
| `openpages.object-manager.validate` | An event is generated when object-manager validate has started. |
| `openpages.process-type.list` | An event is generated when a list of long running process types is fetched. |
| `openpages.workflow-resource.start` | An event is generated when a workflow is started. |
| `openpages.application-text.get` | An event is generated when application text is fetched. |
| `openpages.questionnaire.get` | An event is generated when a questionnaire assessment is fetched. |
| `openpages.user-role-assignment.delete` | An event is generated when a user role is revoked. |
| `openpages.object-type-association.get` | An event is generated when an object type association is fetched. |
| `openpages.user-app-permission.list` | An event is generated when a list of application permissions for a user is fetched. |
| `openpages.resource-lock.set-on` | An event is generated when an object instance is locked. |
| `openpages.app-permission.list` | An event is generated when a list of application permissions is fetched. |
| `openpages.workflow.get` | An event is generated when a workflow definition is fetched. |
| `openpages.process.list` | An event is generated when a list of background processes is fetched. |
| `openpages.resource-permission.get` | An event is generated when an object instance effective permission is fetched. |
| `openpages.role-template.list` | An event is generated when a list of role templates is fetched. |
| `openpages.profile.get` | An event is generated when an object profile is fetched. |
| `openpages.user-impersonate.list` | An event is generated when a user group membership is listed recursively. |
| `openpages.resource.add` | An event is generated when an object instance relationship is added. |
| `openpages.scim-schema.get` | An event is generated when SCIM schema is fetched. |
| `openpages.user.create` | An event is generated when a user is created. |
| `openpages.resource.update` | An event is generated when an object instance is modified. |
| `openpages.tag.list` | An event is generated when tags are listed. |
| `openpages.user-role-assignment.list` | An event is generated when a list of role assignments is fetched. |
| `openpages.process-log.list` | An event is generated when a list of background process logs is fetched. |
| `openpages.folder.list` | An event is generated when folders are listed. |
| `openpages.resource.list` | An event is generated when object instance list is fetched. |
{: caption="Actions that generate API events (UI)" caption-side="bottom"}

## Viewing events
{: #at_ui}

Events that are generated by an instance of the {{site.data.keyword.openpages_short}} service are automatically forwarded to the {{site.data.keyword.logs_full_notm}} service instance that is available in the same [location](/docs/cloud-logs?topic=cloud-logs-regions).

{{site.data.keyword.logs_full_notm}} can have only one instance per location. To view events, you must access the web UI of the {{site.data.keyword.logs_full_notm}} service in the same location where your service instance is available. For more information, see [Launching the UI](/docs/cloud-logs?topic=cloud-logs-instance-launch#instance-launch-cloud-ui).
