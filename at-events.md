---

copyright:
  years: 2023
lastupdated: "2023-10-27"

keywords: audit events in openpages, audit activity in openpages

subcollection: openpages

---
{{site.data.keyword.attribute-definition-list}}

# Auditing events for {{site.data.keyword.openpages_short}}
{: #at_events}

As a security officer, auditor, or manager, you can use the {{site.data.keyword.at_full}} service to track how users and applications interact with the {{site.data.keyword.openpages_short}} service in {{site.data.keyword.cloud_notm}}.
{: shortdesc}

{{site.data.keyword.at_full_notm}} records user-initiated activities that change the state of a service in {{site.data.keyword.cloud_notm}}. You can use this service to investigate abnormal activity and critical actions and to comply with regulatory audit requirements. In addition, you can be alerted about actions as they happen. The events that are collected comply with the Cloud Auditing Data Federation (CADF) standard. For more information, see the [getting started tutorial for {{site.data.keyword.at_full_notm}}](/docs/activity-tracker?topic=activity-tracker-getting-started).

<!-- Choose option 1 or option 2 to document your events -->

<!-- OPTION 1 -->

<!-- Create 3 different sections:
 - A section for platform events, if you're a service that's provisioned in the cloud
 - A section for management events
 - A section for data events  -->

<!-- Replace `service-name` with the name of your service.

## List of platform events
{: #at_actions_platform}

The following table lists the actions that generate an event:


The following table lists the actions that generate an event for managing service credentials that are associated to a service instance:

## List of management events
{: #at_actions}

<!-- Make sure you introduce the table with a detailed description that immediately precedes it.  -

## List of data events
{: #at_actions_data}

<!-- Make sure you introduce the table with a detailed description that immediately precedes it.

<!-- OPTION 2 -->

<!-- If you have multiple events that might not be related, you can create different sections to group them.
-->

<!-- CW: I'm using Option 2 for now-->
<!-- CW: I've hidden global search, Cognos, and LEE -->

The following lists describe {{site.data.keyword.openpages_short}} auditable events.
<!--
When we get descriptions, convert lists to tables:-->

The `update` events do not fill `initialValue` and `newValue` under the `requestData.update` JSON field, unless noted in the event's description. The values are not included to avoid recording sensitive information.
{: note}

## List of platform events
{: #at_actions_platform}

The following table lists the actions on service instances that generate an event:

| Action                                   | Description |
|------------------------------------------|---------|
| `openpages.services.list`                  | An event is generated when the list of service instances is displayed in the Console UI. |
| `openpages.services-filter.list`           | An event is generated when the list of service instances in the Console UI is filtered. |
| `openpages.services.get`                   | An event is generated when service instance details are displayed in the Console UI. |
| `openpages.services-configure.update`      | An event is generated when the configuration settings of a service instance are modified in the Console UI. |
| `openpages.services-eventnotification.update`| An event is generated when the event notification settings for an instance are modified in the Console UI. |
| `openpages.services-transfer-host.update`  | An event is generated when you transfer a custom host name to another instance by using the Console UI. |
| `openpages.services-configure-host.update` | An event is generated when a custom host name is assigned to an instance by using the Console UI. |
| `openpages.services.update`                | An event is generated when an instance is updated. |
| `openpages.services.delete`                | An event is generated when an instance is deleted. |
| `openpages.services.upgrade`               | An event is generated when an instance is upgraded. |
| `openpages.service-allow-list.update`       | An event is generated when the allow list for an instance is updated by using the Console UI. |
| `openpages.service-cpu-metrics.get`       | An event is generated when CPU metrics are retrieved and displayed on the **Usage** tab in the Console UI. |
| `openpages.service-user-metrics.get`      | An event is generated when user metrics are retrieved and displayed on the **Usage** tab in the Console UI. |
| `openpages.service-storage-metrics.get`   | An event is generated when storage metrics are retrieved and displayed on the **Usage** tab in the Console UI. |
| `openpages.service-custom-resource.update`      | An event is generated when a service instance is patched. |
| `openpages.services-sol-usage.update`      | An event is generated when the solution configuration for a service instance is updated. |
| `openpages.services.add`                   | An event is generated when an instance is provisioned. |
| `openpages.services.update`                | An event is generated when you update the properties of an instance. |
| `openpages.services.delete`                | An event is generated when an instance is deleted. |
| `openpages.services-status.enabled`,`disabled`   | An event is generated when a service instance is enabled or disabled, for example, when an instance is deleted by using the Console UI or when an instance is restored by reclamation.  |
| `openpages.services-promoted-component-version.get`  | An event is generated when retrieving the most recent promoted version of a service instance. |
{: caption="Table 1. Actions that generate platform events (UI)" caption-side="bottom"}


## Users, groups, login, and logout events
{: #users-groups}

The following tables list events that are generated when users log in, users log out, and when user management actions occur.

<!-- Saba, please convert these lists into tables. Put x if a description is blank. -->

Login, Logout, Session, Authentication:

| Action:                       | Description:                                                 |
| ----------------------------- | ------------------------------------------------------------ |
| `openpages.user.logoff`         | An event is generated when a user logs out of {{site.data.keyword.openpages_short}}. |
| `openpages.user.logon`         | An event is generated when a user logs in to {{site.data.keyword.openpages_short}}   |
| `openpages.user.session-expire` | An event is generated when a user session expires.           |
{: caption="Table 2. Actions that generate login, logout, session authentication events (UI)" caption-side="bottom"}

User Management:

| Action:                               | Description:                                                          |
| ------------------------------------- | --------------------------------------------------------------------- |
| `openpages.user.get`                    | An event is generated when a user account is fetched.                 |
| `openpages.user.list`                   | An event is generated when user list is fetched.                      |
| `openpages.user.create`                 | An event is generated when a user account is created.                 |
| `openpages.user.update`                 | An event is generated when a user account is modified.                |
| `openpages.user.enable`                 | An event is generated when a user account is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.                |
| `openpages.user.disable`                | An event is generated when a user account is disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.                |
| `openpages.user.lock`                   | An event is generated when a user account is locked.                  |
| `openpages.user.unlock`                 | An event is generated when a user account is unlocked.                |
| `openpages.user-locale.update`          | An event is generated when a user switches locales in IBM OpenPages.  |
| `openpages.user-current-profile.update` | An event is generated when a user switches profiles in IBM OpenPages. |
| `openpages.user-password.update`        | An event is generated when user password is modified                  |
| `openpages.user-preference.set`         | An event is generated when user prefrerence is set                    |
| `openpages.user-association.add`        | An event is generated when user association to a group is added       |
| `openpages.user-association.delete`     | An event is generated when user association to a group is deleted     |
| `openpages.user-association.update`     | An event is generated when user association to a group is replaced    |
{: caption="Table 3. Actions that generate user management events (UI)" caption-side="bottom"}

<!-- `openpages.user-reporting-period.update`
`openpages.user-reporting-period.enable`
The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.
`openpages.user-reporting-period.disable`
The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.
-->

Group Management:

| Action:                                         | Description:                                                                                       |
| ----------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `openpages.group.list`                            | An event is generated when groups are fetched.                                                     |
| `openpages.group.create`                          | An event is generated when a group is created.                                                     |
| `openpages.group.update`                          | An event is generated when a group is updated.                                                     |
| `openpages.group.get`                             | An event is generated when a group is fetched.                                                     |
| `openpages.group-administrator-permission.revoke` | An event is generated when a admistrative permissions are revoked from a group.                    |
| `openpages.group-administrator-permission.assign` | An event is generated when a admistrative permissions are granted to a group.                      |
| `openpages.group-administrator-permission.update` | An event is generated when the admistrative permissions that are assigned to a group are modified. |
| `openpages.group-membership.add`                  | An event is generated when users are added to a group.                                             |
| `openpages.group-membership.remove`               | An event is generated when users are removed from a group.                                         |
| `openpages.group-permission.update`               | An event is generated when the permissions that are assigned to a group are modified.              |
{: caption="Table 4. Actions that generate group management events (UI)" caption-side="bottom"}


## System administration and security events
{: #system-admin}

Audit trail:

| Action:                          | Description:                                                             |
| -------------------------------- | ------------------------------------------------------------------------ |
| `openpages.resource-activity.list` | An event is generated when the Activity tab of a view list is displayed. |
| `openpages.resource-activity.get`  | An event is generated when the Activity tab of a view is displayed.      |
{: caption="Table 5. Actions that generate audit trail events (UI)" caption-side="bottom"}


Currencies:

| Action:                         | Description:                                                           |
| ------------------------------- | ---------------------------------------------------------------------- |
| `openpages.currency.list`         | An event is generated when a currency is listed.                       |
| `openpages.currency.update`       | An event is generated when a currency is updated.                      |
| `openpages.currency.enable`       | An event is generated when a currency is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.                     |
| `openpages.currency.disable`      | An event is generated when a currency is disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.                    |
| `openpages.currency-history.list` | An event is generated when a currency update history is listed.        |
| `openpages.currency.upload`       | An event is generated when currencies are updated by uploading a file. |
{: caption="Table 6. Actions that generate currency events (UI)" caption-side="bottom"}

Encryption keystore:

| Action:                              | Description:                                             |
| ------------------------------------ | -------------------------------------------------------- |
| `openpages.encryption-keystore.get`    | An event is generated when a encryption key is retrived. |
| `openpages.encryption-keystore.enable` | An event is generated when an encryption key is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.         |
| `openpages.encryption-keystore.update` | An event is generated when a encryption key updated.     |
{: caption="Table 7. Actions that generate encryption keystore events (UI)" caption-side="bottom"}


Environment migration:

| Action:                                 | Description:                                                                          |
| --------------------------------------- | ------------------------------------------------------------------------------------- |
| `openpages.configuration.list-import`     | An event is generated when configuration import history is listed in the UI.          |
| `openpages.configuration.submit-import`   | An event is generated when an import is started by using the Import Configuration UI. |
| `openpages.configuration.validate-import` | An event is generated when an import file is validated.                               |
| `openpages.configuration.list-export`     | An event is generated when configuration export history is listed in the UI.          |
| `openpages.configuration.get`             | An event is generated when a configuration export/import item is fetched.             |
| `openpages.configuration.submit-export`   | An event is generated when an export is started by using the Export Configuration UI. |
{: caption="Table 8. Actions that generate environment migration events (UI)" caption-side="bottom"}


Localization \(object text and application text\):

| Action:                             | Description:                                                                    |
| ----------------------------------- | ------------------------------------------------------------------------------- |
| `openpages.object-text.list`          | An event is generated when an object text string list is fetched.               |
| `openpages.object-text.update`        | An event is generated when an object text string is updated.                    |
| `openpages.application-text.update`   | An event is generated when an application text string is updated.               |
| `openpages.application-text-key.list` | An event is generated when a user-defined application text key list is fetched. |
| `openpages.object-text-key.list`      | An event is generated when an object text key string list is fetched.           |
| `openpages.application-text.list`     | An event is generated when an application text string list is fetched.          |
{: caption="Table 9. Actions that generate object text and application text localization events (UI)" caption-side="bottom"}


Logs, processes, trace logs:

| Action:                              | Description:                                                                                                       |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `openpages.log-collector.launch`       | An event is generated when Log Collector is launched from the **Other > Logs** UI.                                      |
| `openpages.log-collector.download-log` | An event is generated when logs that were generated by the Log Collector are downloaded.                           |
| `openpages.process-log.list`           | An event is generated when background process logs are fetched.                                                    |
| `openpages.log-collector.delete-log`   | An event is generated when a Log Collector log file is deleted from the **Other > Logs** UI.                            |
| `openpages.trace-options.list`         | An event is generated when trace oprions are listed in the UI                                                      |
| `openpages.trace-options.update`       | An event is generated when the trace logging settings are updated in the **Other > Logs > System tracing options** UI. |
| `openpages.process.get`                | An event is generated when a background process is fetched.                                                        |
| `openpages.process.list`               | An event is generated when a background process list is fetched.                                                   |
{: caption="Table 10. Actions that generate object text and application text localization events (UI)" caption-side="bottom"}


<!--
- `openpages.cognos-reporting-framework.list`
- `openpages.cognos-reporting-framework.generate`-->

<!--
Reporting periods:

- `openpages.reporting-period.list`
- `openpages.reporting-period.delete`
- `openpages.reporting-period.create`
- `openpages.reporting-period.get`
- `openpages.reporting-period.update`
- `openpages.reporting-period.finalize`
- `openpages.reporting-period.enable`-->

Role templates:

| Action:                                       | Description:                                                                                                 |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| `openpages.role.assign`                         | An event is generated when a role template is assigned to a user or group.                                   |
| `openpages.role.revoke`                         | An event is generated when a role template is removed from a user or group.                                  |
| `openpages.role-template.get`                   | An event is generated when a role template is fetched.                                                       |
| `openpages.role-template.list`                  | An event is generated when a role template list is fetched.                                                  |
| `openpages.role-template.delete`                | An event is generated when a role template is deleted.                                                       |
| `openpages.role-template.enable`                | An event is generated when a role template is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.                                                      |
| `openpages.role-template.disable`               | An event is generated when a role template is disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.                                                     |
| `openpages.role-template.create`                | An event is generated when a role template is created.                                                       |
| `openpages.role-template.lock`                  | An event is generated when a role template is locked.                                                        |
| `openpages.role-template.unlock`                | An event is generated when a role template is unlocked.                                                     |
| `openpages.role-template.update`                | An event is generated when the properties of a role template, such as its Name and Description, are updated. |
| `openpages.role-template-access.add`            | An event is generated when an object type is added to a role template.                                       |
| `openpages.role-template-access.update`         | An event is generated when the access controls for object type are changed for a role template.              |
| `openpages.role-template-access.delete`         | An event is generated when an object type is removed from a role template.                                   |
| `openpages.role-template-app-permission.update` | An event is generated when the application permissions that are assigned to a role template are changed.     |
{: caption="Table 11. Actions that generate role template events (UI)" caption-side="bottom"}


Security rules:

| Action:                                       | Description:                                                                 |
| --------------------------------------------- | ---------------------------------------------------------------------------- |
| `openpages.security-rule.list`                  | An event is generated when a security rules across object types are fetched. |
| `openpages.security-rule.get`                   | An event is generated when a security rules for an object type is fetched.   |
| `openpages.record-level-security-rule.validate` | An event is generated when a record level security rule is validated.        |
| `openpages.record-level-security-rule.create`   | An event is generated when a record level security rule is created.          |
| `openpages.record-level-security-rule.update`   | An event is generated when a record level security rule is modified.         |
| `openpages.record-level-security-rule.enable`   | An event is generated when a record level security rule is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.         |
| `openpages.record-level-security-rule.delete`   | An event is generated when a record level security rule is deleted.          |
| `openpages.field-level-security-rule.validate`  | An event is generated when a field level security rule is validated          |
| `openpages.field-level-security-rule.create`    | An event is generated when a field level security rule is created.           |
| `openpages.field-level-security-rule.update`    | An event is generated when a field level security rule is modified.          |
| `openpages.field-level-security-rule.enable`    | An event is generated when a field level security rule is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.          |
| `openpages.field-level-security-rule.delete`    | An event is generated when a field level security rule is deleted.           |
{: caption="Table 12. Actions that generate security rule events (UI)" caption-side="bottom"}


Settings:

| Action:                      | Description:                                                                |
| ---------------------------- | --------------------------------------------------------------------------- |
| `openpages.setting.get`        | An event is generated when a setting is fetched.                            |
| `openpages.setting.update`     | An event is generated when the value of a setting is modified.              |
| `openpages.setting.create`     | An event is generated when a setting is created.                            |
| `openpages.setting.add-folder` | An event is generated when a custom folder is created on the Settings page. |
| `openpages.setting.copy`       | An event is generated when a setting is copied.                             |
| `openpages.setting.delete`     | An event is generated when a setting is deleted                             |
| `openpages.setting.list`       | An event is generated when settings list is fetched.                        |
{: caption="Table 13. Actions that generate settings events (UI)" caption-side="bottom"}


System admin mode:

| Action:                             | Description:                                              |
| ----------------------------------- | --------------------------------------------------------- |
| `openpages.system-admin-mode.enable`  | An event is generated when System Admin Mode is enabled.  |
| `openpages.system-admin-mode.disable` | An event is generated when System Admin Mode is disabled. |
{: caption="Table 14. Actions that generate system admin mode events (UI)" caption-side="bottom"}


System files:

| Action:                                      | Description:                                                              |
| -------------------------------------------- | ------------------------------------------------------------------------- |
| `openpages.page-and-template.list`             | An event is generated when pages and templates list is fetched.           |
| `openpages.system-file-resource.list`          | An event is generated when system file resource list is fetched.          |
| `openpages.system-file-resource.copy`          | An event is generated when system file resource is copied.                |
| `openpages.system-file-resource.move`          | An event is generated when system file resource is moved.                 |
| `openpages.system-file-resource.delete`        | An event is generated when system file resource is deleted.               |
| `openpages.system-file-resource.rename`        | An event is generated when system file resource is renamed.               |
| `openpages.system-file-resource.get`           | An event is generated when system file resource is fetched.               |
| `openpages.system-file-resource.create`        | An event is generated when system file resource is added.                 |
| `openpages.system-file-resource.update`        | An event is generated when system file resource is modified.              |
| `openpages.system-file-resource-access.list`   | An event is generated when access to the system file resource is listed.  |
| `openpages.system-file-resource-access.update` | An event is generated when access to the system file resource is updated. |
| `openpages.system-file-resource-access.delete` | An event is generated when access to the system file resource is deleted. |
{: caption="Table 15. Actions that generate system files events (UI)" caption-side="bottom"}


## Object types, profiles, schema, object instances events
{: #object-types}

Field dependencies:

| Action:                           | Description:                                               |
| --------------------------------- | ---------------------------------------------------------- |
| `openpages.field-dependency.list`   | An event is generated when field dependencies are listed.  |
| `openpages.field-dependency.create` | An event is generated when a field dependency is created.  |
| `openpages.field-dependency.update` | An event is generated when a field dependency is modified. |
| `openpages.field-dependency.enable` | An event is generated when a field dependency is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
| `openpages.field-dependency.delete` | An event is generated when a field dependency is deleted.  |
{: caption="Table 16. Actions that generate field dependency events (UI)" caption-side="bottom"}

Field groups, fields, and schema:

| Action:                         | Description:                                                              |
| ------------------------------- | ------------------------------------------------------------------------- |
| `openpages.solution.get`          | An event is generated when a solution is fetched.                         |
| `openpages.field-group.list`      | An event is generated when a field group list is fetched                  |
| `openpages.field-group.create`    | An event is generated when a field group is created.                      |
| `openpages.field-group.update`    | An event is generated when a field group is modified.                     |
| `openpages.field-group.delete`    | An event is generated when a field group is deleted.                      |
| `openpages.field-group.add`       | An event is generated when a field group is added to an object type.      |
| `openpages.field-group.remove`    | An event is generated when a field group is removed from an object type.  |
| `openpages.field.list`            | An event is generated when field list is fetched.                         |
| `openpages.field.create`          | An event is generated when a field is created.                            |
| `openpages.field.update`          | An event is generated when a field is modified.                           |
| `openpages.filters.list`          | An event is generated when object filters are listed.                     |
| `openpages.solution-profile.list` | An event is generated when object types with profiles are fetched.        |
| `openpages.object-type.list`      | An event is generated when objec type list is fetched.                    |
| `openpages.object-type.update`    | An event is generated when the properties of an object type are modified. |
{: caption="Table 17. Actions that generate field, field group, and schema events (UI)" caption-side="bottom"}


Filters:

| Action:                        | Description:                                                              |
| ------------------------------ | ------------------------------------------------------------------------- |
| `openpages.object-filter.list`   | An event is generated when object filter list is fetched.                 |
| `openpages.object-filter.get`    | An event is generated when an object filter is fetched.                   |
| `openpages.object-filter.create` | An event is generated when a public filter is defined for an object type. |
| `openpages.object-filter.delete` | An event is generated when a public filter is deleted.                    |
{: caption="Table 18. Actions that generate filter events (UI)" caption-side="bottom"}


Profiles:

| Action:                                | Description:                                                                  |
| -------------------------------------- | ----------------------------------------------------------------------------- |
| `openpages.profile.list`                 | An event is generated when object profiles are listed.                        |
| `openpages.profile.get`                  | An event is generated when an object profile is fetched.                      |
| `openpages.profile.update`               | An event is generated when a profile is modified.                             |
| `openpages.profile.create`               | An event is generated when a profile is created.                              |
| `openpages.profile.enable`               | An event is generated when a profile is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.                             |
| `openpages.profile.delete`               | An event is generated when a profile is deleted.                              |
| `openpages.profile-object-type.list`     | An event is generated when object types for a profile is listed.              |
| `openpages.profile-object-type.delete`   | An event is generated when an object type is removed from a profile           |
| `openpages.profile-object-type.add`      | An event is generated when an object type is added to a profile.              |
| `openpages.profile-actor.list`           | An event is generated when users or groups associated to a profile is listed. |
| `openpages.profile-actor.remove`         | An event is generated when users or groups are removed from a profile.        |
| `openpages.profile-actor.add`            | An event is generated when users or groups are added to a profile.            |
| `openpages.profile-report.delete`        | An event is generated when reports are deleted from a profile.                |
| `openpages.profile-report.add`           | An event is generated when reports are added to a profile.                    |
| `openpages.profile-report.enable`        | An event is generated when reports are enabled on a profile. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.                 |
| `openpages.profile-object-type.get`      | An event is generated when an object type for a profile is fetched.           |
| `openpages.profile-object-field.list`    | An event is generated when object fields for a profile is listed.             |
| `openpages.profile-object-field.delete`  | An event is generated when an object field is removed from a profile.         |
| `openpages.profile-object-field.add`     | An event is generated when an object field is added to a profile.             |
| `openpages.profile-object-field.update`  | An event is generated when an object field is modified on a profile.          |
| `openpages.profile-object-filter.delete` | An event is generated when a public filter is removed from a profile.         |
| `openpages.profile-object-filter.add`    | An event is generated when a public filter is added to a profile.             |
{: caption="Table 19. Actions that generate profile events (UI)" caption-side="bottom"}


Objects:

| Action:                              | Description:                                                                  |
| ------------------------------------ | ----------------------------------------------------------------------------- |
| `openpages.resource.get`               | An event is generated when an object instance is fetched to a task view.      |
| `openpages.file-resource-version.list` | An event is generated when an attachment versions are fetched to a task view. |
| `openpages.resource.update`            | An event is generated when an object instance is modified.                    |
| `openpages.resource.bulk-update`       | An event is generated when object instances are updated by a bulk operation.  |
| `openpages.file-resource.update`       | An event is generated when an attachment is modified.                         |
| `openpages.resource.create`            | An event is generated when an object instance is created.                     |
| `openpages.file-resource.create`       | An event is generated when an attachment is created.                          |
| `openpages.resource.delete`            | An event is generated when an object instance is deleted.                     |
| `openpages.resource.lock`              | An event is generated when an object instance is locked.                      |
| `openpages.resource.unlock`            | An event is generated when an object instance is unlocked.                    |
| `openpages.resource.search`            | An event is generated when global search query is issued.                     |
| `openpages.resource.move`              | An event is generated when an object instance is moved.                       |
| `openpages.resource.list`              | An event is generated when object instance list is fetched.                   |
| `openpages.resource.export`            | An event is generated when object instance list is exported.                  |
{: caption="Table 20. Actions that generate object events (UI)" caption-side="bottom"}


Object resets:

| Action:                      | Description:                                                              |
| ---------------------------- | ------------------------------------------------------------------------- |
| `openpages.object-reset.get`   | An event is generated when an object-reset operation result is fetched.   |
| `openpages.object-reset.list`  | An event is generated when object-reset operation result list is fetched. |
| `openpages.object-reset.start` | An event is generated when object-reset operation is started.             |
{: caption="Table 21. Actions that generate object reset events (UI)" caption-side="bottom"}


Object type associations:

| Action:                                    | Description:                                                                   |
| ------------------------------------------ | ------------------------------------------------------------------------------ |
| `openpages.object-relationship.list`         | An event is generated when object type relationships are listed.               |
| `openpages.resource.add`                     | An event is generated when an object instance relationship is added.           |
| `openpages.resource.remove-all`              | An event is generated when all the object instance relationships are removed.  |
| `openpages.resource.remove`                  | An event is generated when an object instance relationship is removed.         |
| `openpages.resource.copy`                    | An event is generated when an object instances are copied recursively.         |
| `openpages.resource-primary-parent.reassign` | An event is generated when an object primary parent is reassigned.             |
| `openpages.object-relationship.enable`       | An event is generated when an object type relationship is enabled or disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
| `openpages.object-relationship.update`       | An event is generated when an object type relationship is updated.             |
{: caption="Table 22. Actions that generate object type associations events (UI)" caption-side="bottom"}


Recursive object types:

| Action:                                 | Description:                                                       |
| --------------------------------------- | ------------------------------------------------------------------ |
| `openpages.recursive-object-level.list`   | An event is generated when recursive object level list is fetched. |
| `openpages.recursive-object-level.create` | An event is generated when recursive object level is created.      |
| `openpages.recursive-object-level.delete` | An event is generated when recursive object level is deleted.      |
{: caption="Table 23. Actions that generate recursive object type events (UI)" caption-side="bottom"}


Solutions:

| Action:                          | Description:                                                  |
| -------------------------------- | ------------------------------------------------------------- |
| `openpages.solution.list`          | An event is generated when solutions are listed.              |
| `openpages.solution.create`        | An event is generated when a solution is created.             |
| `openpages.solution.update`        | An event is generated when a solution is updated.             |
| `openpages.solution.delete`        | An event is generated when a solution is deleted.             |
| `openpages.field-exclusion.list`   | An event is generated when a field exclusion list is fetched. |
| `openpages.field-exclusion.create` | An event is generated when a field exclusion is created.      |
| `openpages.field-exclusion.update` | An event is generated when a field exclusion is updated.      |
| `openpages.field-exclusion.delete` | An event is generated when a field exclusion is deleted.      |
{: caption="Table 24. Actions that generate solution events (UI)" caption-side="bottom"}


## Calculations, workflows, views, and other user interface events
{: #calc-workflow}

Calculations:

| Action:                             | Description:                                                          |
| ----------------------------------- | --------------------------------------------------------------------- |
| `openpages.calculation.list`          | An event is generated when calculations list is fetched.              |
| `openpages.calculation.get`           | An event is generated when a calculation is fetched.                  |
| `openpages.calculation.create`        | An event is generated when a calculation is created.                  |
| `openpages.calculation.update`        | An event is generated when a calculation is updated.                  |
| `openpages.calculation.publish`       | An event is generated when a calculation is published.                |
| `openpages.calculation.discard-draft` | An event is generated when a draft calculation is discarded.          |
| `openpages.calculation.delete`        | An event is generated when a calculation is deleted.                  |
| `openpages.calculation.enable`        | An event is generated when a calculation is enabled or disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.     |
| `openpages.bulk-calculation.start`    | An event is generated when a calculation is run for object instances. |
{: caption="Table 25. Actions that generate calculation events (UI)" caption-side="bottom"}


Dashboards:

| Action:                                 | Description:                                                                   |
| --------------------------------------- | ------------------------------------------------------------------------------ |
| `openpages.admin-dashboard.list`          | An event is generated when administrative dashboard list is fetched.           |
| `openpages.admin-dashboard.create`        | An event is generated when an administrative dashboard is created.             |
| `openpages.admin-dashboard.get`           | An event is generated when an administrative dashboard is fetched.             |
| `openpages.admin-dashboard.update`        | An event is generated when an administrative dashboard is updated.             |
| `openpages.admin-dashboard.publish`       | An event is generated when an administrative dashboard is published.           |
| `openpages.admin-dashboard.discard-draft` | An event is generated when an administrative dashboard draft is discarded.     |
| `openpages.admin-dashboard.delete`        | An event is generated when an administrative dashboard is deleted.             |
| `openpages.admin-dashboard.enable`        | An event is generated when an administrative dashboard is enabled or disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
| `openpages.user-dashboard.load`           | An event is generated when a user dashboard is loaded.                         |
| `openpages.user-dashboard.update`         | An event is generated when a user dashboard is updated.                        |
{: caption="Table 26. Actions that generate dashboard events (UI)" caption-side="bottom"}


FastMap:

| Action:                    | Description:                                                       |
| -------------------------- | ------------------------------------------------------------------ |
| `openpages.fastmap.validate` | An event is generated when an import file is validated by FastMap. |
| `openpages.fastmap.import`   | An event is generated when a FastMap import is started.            |
{: caption="Table 27. Actions that generate FastMap events (UI)" caption-side="bottom"}


File attachments:

| Action:                                 | Description:                                                    |
| --------------------------------------- | --------------------------------------------------------------- |
| `openpages.file-resource.download`        | An event is generated when an attachment is downloaded.         |
| `openpages.file-resource.checkout`        | An event is generated when an attachment is checked out.        |
| `openpages.file-resource.checkin`         | An event is generated when an attachment is checked in.         |
| `openpages.file-resource.cancel-checkout` | An event is generated when an attachment checkout is canceled.  |
| `openpages.file-type.create`              | An event is generated when an attachment file type is created.  |
| `openpages.file-type.disable`             | An event is generated when an attachment file type is disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
| `openpages.file-type.enable`              | An event is generated when an attachment file type is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
{: caption="Table 28. Actions that generate file attachment events (UI)" caption-side="bottom"}


<!-- - `openpages.file-type.enable-search`-->
<!--
Global search:
{: #global-search}
- `openpages.search-config.list`
- `openpages.search-config.update`-->

Folders:

| Action:                          | Description:                                    |
| -------------------------------- | ----------------------------------------------- |
| `openpages.folder-resource.create` | An event is generated when a folder is created. |
| `openpages.folder-resource.delete` | An event is generated when a folder is deleted. |
{: caption="Table 29. Actions that generate folder events (UI)" caption-side="bottom"}


Net Promoter Score \(NPS\):

| Action:                       | Description:                                                                      |
| ----------------------------- | --------------------------------------------------------------------------------- |
| `openpages.nps-settings.get`    | An event is generated when the settings for Net Promoter Score (NPS) is fetched.  |
| `openpages.nps-settings.update` | An event is generated when the settings for Net Promoter Score (NPS) are updated. |
{: caption="Table 30. Actions that generate Net Promoter Score events (UI)" caption-side="bottom"}


Questionnaires:

| Action:                                              | Description:                                                                                            |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `openpages.questionnaire-template.get`                 | An event is generated when a questionnaire template is fetched.                                         |
| `openpages.questionnaire-template.add-default-objects` | An event is generated when default section, subsection, question are added to a questionnaire template. |
| `openpages.questionnaire-template.copy-from-existing`  | An event is generated when a copy of questionnaire template is created.                                 |
| `openpages.questionnaire-template.update`              | An event is generated when a questionnaire template is updated.                                         |
| `openpages.questionnaire.copy-answers`                 | An event is generated when questionnaire assessment answers are copied from a source assessment.        |
| `openpages.questionnaire-template.reorder`             | An event is generated when questions are reorded in a questionnaire template.                           |
| `openpages.questionnaire.upload-attachment`            | An event is generated when attachment is added to a questionnaire assessment.                           |
| `openpages.questionnaire.get`                          | An event is generated when a questionnaire assessment is fetched.                                       |
{: caption="Table 31. Actions that generate questionnaire events (UI)" caption-side="bottom"}


Rules \(Regulatory Event rules\):

| Action:               | Description:                                                                    |
| --------------------- | ------------------------------------------------------------------------------- |
| `openpages.rule.get`    | An event is generated when a regulatory event rule is fetched.                  |
| `openpages.rule.create` | An event is generated when a rule is created in the Regulatory Event Rules UI.  |
| `openpages.rule.update` | An event is generated when a rule in the Regulatory Event Rules UI is modified. |
| `openpages.rule.delete` | An event is generated when a rule in the Regulatory Event Rules UI is deleted.  |
| `openpages.rule.enable` | An event is generated when a rule in the Regulatory Event Rules UI is enabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
| `openpages.rule.list`   | An event is generated when rules in the Regulatory Event Rules UI is fetched.   |
{: caption="Table 32. Actions that generate rule events in the Regulatory Event Rules (UI)" caption-side="bottom"}


Scheduler jobs:

| Action:                          | Description:                                                       |
| -------------------------------- | ------------------------------------------------------------------ |
| `openpages.scheduler-job.get`      | An event is generated when a scheduler job is fetched.             |
| `openpages.scheduler-job-log.list` | An event is generated when a job execution log is viewed.          |
| `openpages.scheduler-job.list`     | An event is generated when scheduler job list is fetched.          |
| `openpages.scheduled-job.create`   | An event is generated when a scheduler job is created.             |
| `openpages.scheduled-job.update`   | An event is generated when a scheduler job is updated.             |
| `openpages.scheduled-job.enable`   | An event is generated when a scheduler job is enabled or disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
| `openpages.scheduled-job.start`   | An event is generated when a scheduler job is started.             |
| `openpages.scheduled-job.delete`   | An event is generated when a scheduler job is deleted.             |
{: caption="Table 33. Actions that generate schedular job events (UI)" caption-side="bottom"}

Tags:

| Action:                          | Description:                                                     |
| -------------------------------- | ---------------------------------------------------------------- |
| `openpages.tag.list`               | An event is generated when tags are listed.                      |
| `openpages.tag.create`             | An event is generated when a tag is created.                     |
| `openpages.tag.update`             | An event is generated when the properties of a tag are modified. |
| `openpages.tag.enable`             | An event is generated when a tag is enabled or disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.        |
| `openpages.tag-association.get`    | An event is generated when tags for a resource is fetched.       |
| `openpages.tag-association.add`    | An event is generated when tags for a resource is added.         |
| `openpages.tag-association.delete` | An event is generated when tags for a resource is deleted.       |
| `openpages.tag-association.update` | An event is generated when tags for a resource is updated.       |
{: caption="Table 34. Actions that generate tag events (UI)" caption-side="bottom"}

Themes:

| Action:                | Description:                                               |
| ---------------------- | ---------------------------------------------------------- |
| `openpages.theme.list`   | An event is generated when themes are listed               |
| `openpages.theme.create` | An event is generated when a theme is created.             |
| `openpages.theme.get`    | An event is generated when a theme is fetched.             |
| `openpages.theme.update` | An event is generated when a theme is updated.             |
| `openpages.theme.delete` | An event is generated when a theme is deleted.             |
| `openpages.theme.enable` | An event is generated when a theme is enabled or disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field. |
{: caption="Table 35. Actions that generate theme events (UI)" caption-side="bottom"}

Workflows:

| Action:                                     | Description:                                                                |
| ------------------------------------------- | --------------------------------------------------------------------------- |
| `openpages.workflow.get`                      | An event is generated when a workflow definition is fetched.                |
| `openpages.workflow.create`                   | An event is generated when a workflow definition is created.                |
| `openpages.workflow.update`                   | An event is generated when a workflow definition is updated.                |
| `openpages.workflow.publish`                  | An event is generated when a workflow definition is published.              |
| `openpages.workflow.delete`                   | An event is generated when a workflow definition is deleted.                |
| `openpages.workflow.enable`                   | An event is generated when a workflow definition is enabled or disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.   |
| `openpages.workflow.list`                     | An event is generated when a workflow definitions are listed.               |
| `openpages.workflow.discard-draft`            | An event is generated when a draft of workflow definition is discarded.     |
| `openpages.workflow-resorce.synchronize`      | An event is generated when a workflow is synchronized.                      |
| `openpages.workflow-resource.list`            | An event is generated when workflows are listed.                            |
| `openpages.workflow-resource.terminate`       | An event is generated when workflows are terminated.                        |
| `openpages.workflow-resource.validate-action` | An event is generated when a workflow action is validated.                  |
| `openpages.workflow-resource.bulk-start`      | An event is generated when workflows are started for a workflow definition. |
| `openpages.resource-workflow-action.bulk-run` | An event is generated when workflow action is processed in bulk             |
| `openpages.resource-workflow-action.run`      | An event is generated when a workflow action is processed.                  |
| `openpages.resource-workflow.start`           | An event is generated when a workflow is started.                           |
{: caption="Table 36. Actions that generate workflow events (UI)" caption-side="bottom"}

Views:

| Action:                      | Description:                                                    |
| ---------------------------- | --------------------------------------------------------------- |
| `openpages.view.list`          | An event is generated when views are listed.                    |
| `openpages.view.get`           | An event is generated when a view is fetched.                   |
| `openpages.view.create`        | An event is generated when a view is created.                   |
| `openpages.view.update`        | An event is generated when a view is modified.                  |
| `openpages.view.validate`      | An event is generated when a view is validated.                 |
| `openpages.view.publish`       | An event is generated when a view is published.                 |
| `openpages.view.delete`        | An event is generated when a view is deleted.                   |
| `openpages.view.discard-draft` | An event is generated when the changes to a view are discarded. |
| `openpages.view.enable`        | An event is generated when a view is enabled or disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.      |
| `openpages.admin-view.create`  | An event is generated when an admin view is created.            |
{: caption="Table 37. Actions that generate view events (UI)" caption-side="bottom"}

<!--
| `openpages.view.disable`        | An event is generated when a view is disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.      |
| `openpages.encryption-keystore.disable` | An event is generated when an encryption key is disabled. The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.         |



-->

<!--## Loss Event Entry
{: #Loss-event-entry}

Loss Event Entry app:

- `openpages.lossevent.create`
- `openpages.lossevent.invalid-access`
- `openpages.lossevent-resource.create`
- `openpages.lossevent-file-resource.create`

Loss Event Entry configuration:

- `openpages.lossevent-config.update`
- `openpages.lossevent-config.validate`
- `openpages.questionnaire-program.launch`-->

## Integration-related events
{: #integrations}

AI models:

| Action:                                   | Description:                                                       |
| ----------------------------------------- | ------------------------------------------------------------------ |
| `openpages.ai-model-configuration.list`     | An event is generated when AI model configurations are listed.     |
| `openpages.ai-model-configuration.get`      | An event is generated when an AI model configurations is fetched.  |
| `openpages.ai-model-configuration.create`   | An event is generated when an AI model configuration is created.   |
| `openpages.ai-model-configuration.update`   | An event is generated when an AI model configuration is updated.   |
| `openpages.ai-model-configuration.delete`   | An event is generated when an AI model configuration is deleted.   |
| `openpages.ai-model-configuration.validate` | An event is generated when an AI model configuration is validated. |
| `openpages.ai-model.suggest-insight`        | An event is generated when an AI model suggests an insight.        |
{: caption="Table 38. Actions that generate AI model events (UI)" caption-side="bottom"}

<!--
Cognos:

- `openpages.cognos.enable` The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.
- `openpages.cognos.disable` The `true` or `false` values are populated to the `initialValue` and `newValue` fields under the `requestData.update` JSON field.
- `openpages.computed-field.execute`
- `openpages.report-fragment.execute`
- `openpages.reporting-schema.list`
- `openpages.reporting-schema.create`
- `openpages.reporting-schema.recreate`
- `openpages.reporting-schema.enable`
- `openpages.reporting-schema.disable`
- `openpages.reporting-schema.drop`
- `openpages.reporting-schema.update`
- `openpages.report.execute`
- `openpages.report.publish`-->

Classifiers:

| Action:                              | Description:                                                 |
| ------------------------------------ | ------------------------------------------------------------ |
| `openpages.watson-classifier.create`   | An event is generated when a watson classifier is created.   |
| `openpages.watson-classifier.update`   | An event is generated when a watson classifier is updated.   |
| `openpages.watson-classifier.delete`   | An event is generated when a watson classifier is deleted.   |
| `openpages.watson-classifier.validate` | An event is generated when a watson classifier is validated. |
{: caption="Table 39. Actions that generate watson classifier events (UI)" caption-side="bottom"}

Microsoft Office:

| Action:                          | Description:                                                                 |
| -------------------------------- | ---------------------------------------------------------------------------- |
| `openpages.msoffice-resource.edit` | An event is generated when microsoft office file editing session is started. |
| `openpages.msoffice-resource.save` | An event is generated when microsoft office file is saved.                   |
{: caption="Table 40. Actions that generate Microsoft Office events (UI)" caption-side="bottom"}

watsonx Assistant:

| Action:                              | Description:                                                              |
| ------------------------------------ | ------------------------------------------------------------------------- |
| `openpages.watson-assistant.get`       | An event is generated when a watson assistant configuration is fetched.   |
| `openpages.watson-assistant.validate`  | An event is generated when a watson assistant configuration is validated. |
| `openpages.watson-assistant.configure` | An event is generated when a watson assistant is configured.              |
{: caption="Table 41. Actions that generate watsonx Assistant events (UI)" caption-side="bottom"}

Watson Language Translator:

| Action:                                      | Description:                                                             |
| -------------------------------------------- | ------------------------------------------------------------------------ |
| `openpages.watson-translator.get`              | An event is generated when Watson Translator configuration is fetched.    |
| `openpages.watson-translator.update`           | An event is generated when Watson Translator configuration is updated.    |
| `openpages.watson-translator.validate`         | An event is generated when Watson Translator configuration is validated. |
| `openpages.watson-translator.translate`        | An event is generated when Watson Translator translates a text.           |
| `openpages.watson-translator.translate-object` | An event is generated when Watson Translator translates object texts.    |
| `openpages.watson-translator.translate-view`   | An event is generated when Watson Translator translates view labels.     |
{: caption="Table 42. Actions that generate Watson Language Translator events (UI)" caption-side="bottom"}

## Feed provider events
{: #feeds}

Reg-Track:

| Action:                    | Description:                                                          |
| -------------------------- | --------------------------------------------------------------------- |
| `openpages.reg-track.import` | An event is generated when a reg-track feed is imported.              |
| `openpages.reg-track.get`    | An event is generated when a reg-track feed configuration is fetched. |
| `openpages.reg-track.update` | An event is generated when a reg-track feed configuration is updated. |
{: caption="Table 43. Actions that generate reg-track feed events (UI)" caption-side="bottom"}

Thomson Reuters:

| Action:                             | Description:                                                                    |
| ----------------------------------- | ------------------------------------------------------------------------------- |
| `openpages.taxonomy-mapping.download` | An event is generated when Thomson Reuters feed taxonomy mapping is downloaded. |
| `openpages.taxonomy-mapping.update`   | An event is generated when Thomson Reuters feed taxonomy mapping is updated.    |
| `openpages.trri.import`               | An event is generated when Thomson Reuters feed is imported.                    |
| `openpages.trri.get`                  | An event is generated when Thomson Reuters feed configuration is fetched.       |
| `openpages.trri.update`               | An event is generated when Thomson Reuters feed configuration is updated.       |
{: caption="Table 44. Actions that generate Thomson Reuters feed events (UI)" caption-side="bottom"}

Wolters Kluwer:

| Action:             | Description:                                                             |
| ------------------- | ------------------------------------------------------------------------ |
| `openpages.wk.import` | An event is generated when Wolters Kluwer feed is imported.              |
| `openpages.wk.get`    | An event is generated when Wolters Kluwer feed configuration is fetched. |
| `openpages.wk.update` | An event is generated when Wolters Kluwer feed configuration is updated. |
{: caption="Table 45. Actions that generate Wolters Kluwer feed events (UI)" caption-side="bottom"}

## API events
{: #api-events}

| Action:                                       | Description:                                                                             |
| --------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `openpages.application-text.get`                | An event is generated when application text is fetched.                                  |
| `openpages.application-text.list`               | An event is generated when application text are listed.                                  |
| `openpages.app-permission.get`                  | An event is generated when an application permission is fetched.                         |
| `openpages.app-permission.list`                 | An event is generated when application permissions are listed.                           |
| `openpages.base-currency.get`                   | An event is generated when base currency is fetched.                                     |
| `openpages.configuration.decrypt`               | An event is generated when sensitive data decrypt operation is started.                  |
| `openpages.configuration.encrypt`               | An event is generated when sensitive data encrypt operation is started.                  |
| `openpages.currency.get`                        | An event is generated when a currency is fetched.                                        |
| `openpages.currency.list`                       | An event is generated when currencies are listed.                                        |
| `openpages.currency.update`                     | An event is generated when a currency is updated.                                        |
| `openpages.exchange-rate.bulk-update`           | An event is generated when exchange rates are updated in bulk.                           |
| `openpages.exchange-rate.list`                  | An event is generated when exchange rates are listed.                                    |
| `openpages.exchange-rate.update`                | An event is generated when an exchange rate is updated.                                  |
| `openpages.file-resource.get`                   | An event is generated when an attachment is fetched.                                     |
| `openpages.file-resource.update`                | An event is generated when an attachment is updated.                                     |
| `openpages.folder.create`                       | An event is generated when a folder is created.                                          |
| `openpages.folder.get`                          | An event is generated when a folder is fetched.                                          |
| `openpages.folder.list`                         | An event is generated when folders are listed.                                           |
| `openpages.folder.update`                       | An event is generated when a folder is updated.                                          |
| `openpages.folder-permission.get`               | An event is generated when folder permissions are fetched.                               |
| `openpages.folder-template.get`                 | An event is generated when a folder template is fetched.                                 |
| `openpages.group.add`                           | An event is generated when a user group is added.                                        |
| `openpages.group.get`                           | An event is generated when a user group is fetched.                                      |
| `openpages.group.list`                          | An event is generated when a user group is listed.                                       |
| `openpages.group.update`                        | An event is generated when a user group is updated.                                      |
| `openpages.group-member.add`                    | An event is generated when a user added to a group .                                     |
| `openpages.group-member.delete`                 | An event is generated when a user removed from a group.                                  |
| `openpages.group-member.list`                   | An event is generated when a group members are listed.                                   |
| `openpages.group-permission.list`               | An event is generated when group permissions are listed.                                 |
| `openpages.group-role-assignment.add`           | An event is generated when a role is assigned to a group.                                |
| `openpages.group-role-assignment.delete`        | An event is generated when a role is removed from a group.                               |
| `openpages.group-role-assignment.list`          | An event is generated when role assignments for a group is listed.                       |
| `openpages.object-manager.fetch-dump`           | An event is generated when ObjectManager dump is fetched.                                |
| `openpages.object-manager.get-load-log`         | An event is generated when ObjectManager load logs are fetched.                          |
| `openpages.object-manager.get-validate-log`     | An event is generated when ObjectManager validate logs are fetched.                      |
| `openpages.object-manager.submit-dump`          | An event is generated when ObjectManager dump is started.                                |
| `openpages.object-manager.submit-load`          | An event is generated when ObjectManager load is started.                                |
| `openpages.object-manager.submit-validate`      | An event is generated when ObjectManager validate is started.                            |
| `openpages.object-manager.upload-load-data`     | An event is generated when ObjectManager load data is uploaded.                          |
| `openpages.object-manager.upload-validate-data` | An event is generated when ObjectManager validate data is uploaded.                      |
| `openpages.object-type.get`                     | An event is generated when an object type is fetched.                                    |
| `openpages.object-type.list`                    | An event is generated when object types are listed.                                      |
| `openpages.object-type-association.get`         | An event is generated when an object type association is fetched.                        |
| `openpages.object-type-association.list`        | An event is generated when object type associtions are listed.                           |
| `openpages.process.get`                         | An event is generated when a long running process is fetched.                            |
| `openpages.process.list`                        | An event is generated when long running processes are listed.                            |
| `openpages.process.terminate`                   | An event is generated when a long running process is terminated.                         |
|`openpages.process-log.list`                    | An event is generated when long running process logs are fetched.                        |
| `openpages.process-type.list`                   | An event is generated when long running process types are listed.                        |
| `openpages.profile.get`                         | An event is generated when an object profile is fetched.                                 |
| `openpages.profile.list`                        | An event is generated when object profiles are listed.                                   |
| `openpages.profile-object-field.list`           | An event is generated when object profile fields are listed.                             |
| `openpages.query.execute`                       | An event is generated when query API is executed.                                        |
| `openpages.questionnaire.get`                   | An event is generated when a questionnaire is fetched.                                   |
| `openpages.resource.add`                        | An event is generated when an object instance is created.                                |
| `openpages.resource.associate`                  | An event is generated when object instance is associated to parent or child.             |
| `openpages.resource.copy`                       | An event is generated when an object instance is copied recursively.                     |
| `openpages.resource.delete`                     | An event is generated when an object instance is deleted.                                |
| `openpages.resource.get`                        | An event is generated when an object instance is fetched.                                |
| `openpages.resource.list`                       | An event is generated when object instances are listed.                                  |
| `openpages.resource.lock`                       | An event is generated when an object instance is locked.                                 |
| `openpages.resource.move`                       | An event is generated when an object instance is moved recursively.                      |
| `openpages.resource.unlock`                     | An event is generated when an object instance is unlocked.                               |
| `openpages.resource.unlock-descendants`         | An event is generated when an object instance is unlocked recursively.                   |
| `openpages.resource.update`                     | An event is generated when an object instance is updated.                                |
| `openpages.resource-activity.list`              | An event is generated when an object instance activities are listed.                     |
| `openpages.resource-association.delete`         | An event is generated when an object instance is disassociated from a parent or a child. |
| `openpages.resource-association.get`            | An event is generated when an object instance association is fetched.                    |
| `openpages.resource-association.list`           | An event is generated when object instance associations are listed.                      |
| `openpages.resource-permission.get`             | An event is generated when an object instance effective permission is fetched.           |
| `openpages.resource-template.get`               | An event is generated when an empty object instance template is fetched.                 |
| `openpages.role-template.get`                   | An event is generated when a role template is fetched.                                   |
| `openpages.role-template.list`                  | An event is generated when role templates are listed.                                    |
| `openpages.role-template-access.list`           | An event is generated when accesses to a role template is listed.                        |
| `openpages.role-template-app-permission.list`   | An event is generated when application permissions of a role template is listed.         |
| `openpages.root-folder.get`                     | An event is generated when root folders of object types are fetched.                     |
| `openpages.setting.get`                         | An event is generated when a setting is fetched.                                         |
| `openpages.setting.list`                        | An event is generated when a setting is listed.                                          |
| `openpages.sub-group.add`                       | An event is generated when a group member is added to a group.                           |
| `openpages.sub-group.delete`                    | An event is generated when a group member is removed from a group.                       |
| `openpages.sub-group.list`                      | An event is generated when group members of a group is listed.                           |
| `openpages.system-admin-mode.get`               | An event is generated when system admin mode flag is fetched.                            |
| `openpages.system-admin-mode.update`            | An event is generated when system admin mode flag is updated.                            |
| `openpages.tag.add`                             | An event is generated when a tag is added.                                               |
| `openpages.tag.get`                             | An event is generated when a tag is fetched.                                             |
| `openpages.tag.list`                            | An event is generated when tags are listed.                                              |
| `openpages.tag.update`                          | An event is generated when tags are updated.                                             |
| `openpages.tag-association.add`                 | An event is generated when tags are associated to an object instance.                    |
| `openpages.tag-association.delete`              | An event is generated when tags are disassociated from an object instance.               |
| `openpages.tag-association.list`                | An event is generated when associated tags are listed for an object instance.            |
| `openpages.trace-options.update`                | An event is generated when trace options are updated.                                    |
| `openpages.user.add`                            | An event is generated when an user is created.                                           |
| `openpages.user.anonymize`                      | An event is generated when user attributes are anonymized.                               |
| `openpages.user.get`                            | An event is generated when an user details are fetched.                                  |
| `openpages.user.update`                         | An event is generated when an user detail is updated.                                    |
| `openpages.user-app-permission.list`            | An event is generated when application permissions of a user is listed.                  |
| `openpages.user-impersonate.list`               | An event is generated when a user group membership is listed recursively.                |
| `openpages.user-membership.list`                | An event is generated when a user group membership is listed.                            |
| `openpages.user-password.reset`                 | An event is generated when a user password is reset.                                     |
| `openpages.user-role-assignment.add`            | An event is generated when a role is assigned to a user.                                 |
| `openpages.user-role-assignment.delete`         | An event is generated when a user role is revoked.                                       |
| `openpages.user-role-assignment.lis`t           | An event is generated when a user roles are listed.                                      |
{: caption="Table 46. Actions that generate API events (UI)" caption-side="bottom"}

 <!---
`openpages.cognos.integrate
`openpages.current-reporting-period.get`
`openpages.report-fragment.execute`
`openpages.reporting-period.get`
`openpages.reporting-period.list``-->

## Viewing events
{: #at_ui}

<!-- As in the previous section, there are multiple options. Choose the one that best suits your service, and delete the other ones. -->

<!-- Option 1: Global service: A service is global when events are generated and available through the global AT domain, For example, IAM, BSS, account management -->

<!-- Option 2: Location based service: A location-based service generates events in the same location where the service instance is provisioned. For example, Certificate Manager. -->

Events that are generated by an instance of the {{site.data.keyword.openpages_short}} service are automatically forwarded to the {{site.data.keyword.at_full_notm}} service instance that is available in the same location.

{{site.data.keyword.at_full_notm}} can have only one instance per location. To view events, you must access the web UI of the {{site.data.keyword.at_full_notm}} service in the same location where your service instance is available. For more information, see [Launching the UI](/docs/activity-tracker?topic=activity-tracker-launch).

<!--
## Analyzing events
{: #at_events_iam_analyze}

List events in your service that add additional information in requestData and responseData. -->

<!-- Provide information about the events in your service that add additional information in requestData and responseData. See the IAM Events topic for a sample topic that includes this section: /docs/activity-tracker?topic=activity-tracker-at_events_iam#at_events_iam_analyze.  -->
