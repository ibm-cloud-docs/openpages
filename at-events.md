---

copyright:
  years: 2023
lastupdated: "2023-09-21"

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

Login, Logout, Session, Authentication:

- `openpages.user.logoff`   An event is generated when a user logs out of {{site.data.keyword.openpages_short}}.
- `openpages.user.logon`    An event is generated when a user logs in to {{site.data.keyword.openpages_short}}
- `openpages.user.session-expire`   An event is generated when a user session expires.

User Management:

- `openpages.user.get`
- `openpages.user.list`
- `openpages.user.create`   An event is generated when a user account is created.
- `openpages.user.update`   An event is generated when a user account is modified.
- `openpages.user.enable`   An event is generated when a user account is enabled.
- `openpages.user.disable`  An event is generated when a user account is disabled.
- `openpages.user.lock`    An event is generated when a user account is locked.
- `openpages.user.unlock`   An event is generated when a user account is unlocked.
- `openpages.user-locale.update`   An event is generated when a user switches locales in {{site.data.keyword.openpages_short}}.
- `openpages.user-current-profile.update`   An event is generated when a user switches profiles in {{site.data.keyword.openpages_short}}.
- `openpages.user-password.update`
- `openpages.user-preference.set`
- `openpages.user-association.add`
- `openpages.user-association.delete`
- `openpages.user-association.update`

<!-- `openpages.user-reporting-period.update`-->

Group Management:

- `openpages.group.list`
- `openpages.group.create`   An event is generated when a group is created.
- `openpages.group.update`   An event is generated when a group is updated.
- `openpages.group.get`
- `openpages.group-administrator-permission.revoke`  An event is generated when a admistrative permissions are revoked from a group.
- `openpages.group-administrator-permission.assign`  An event is generated when a admistrative permissions are granted to a group.
- `openpages.group-administrator-permission.update`  An event is generated when the admistrative permissions that are assigned to a group are modified.
- `openpages.group-membership.add`   An event is generated when users are added to a group.
- `openpages.group-membership.remove`   An event is generated when users are removed from a group.
- `openpages.group-permission.update`   An event is generated when the permissions that are assigned to a group are modified.

## System administration and security events
{: #system-admin}

Audit trail:

- `openpages.resource-activity.list`
- `openpages.resource-activity.get`   An event is generated when the **Activity** tab of a view is displayed.

Currencies:

- `openpages.currency.list`
- `openpages.currency.update`
- `openpages.currency.enable`   An event is generated when a currency is enabled.
- `openpages.currency.disable`   An event is generated when a currency is disabled.
- `openpages.currency-history.list`
- `openpages.currency.upload`   An event is generated when currencies are updated by uploading a file.

Encryption keystore:

- `openpages.encryption-keystore.get`
- `openpages.encryption-keystore.enable`
- `openpages.encryption-keystore.update`

Environment migration:

- `openpages.configuration.list-import`
- `openpages.configuration.submit-import`   An event is generated when an import is started by using the Import Configuration UI.
- `openpages.configuration.validate-import`  An event is generated when an import file is validated.
- `openpages.configuration.list-export`
- `openpages.configuration.get`
- `openpages.configuration.submit-export`   An event is generated when an export is started by using the Export Configuration UI.

Localization \(object text and application text\):

- `openpages.object-text.list`
- `openpages.object-text.update`   An event is generated when an object text string is updated.
- `openpages.application-text.update`   An event is generated when an application text string is updated.
- `openpages.application-text-key.list`   An event is generated when a user-defined application text key is created.
- `openpages.object-text-key.list`
- `openpages.application-text.list`

Logs, processes, trace logs:

- `openpages.log-collector.launch`   An event is generated when Log Collector is launched from the **Other> Logs** UI.
- `openpages.log-collector.download-log`   An event is generated when logs that were generated by the Log Collector are downloaded.
- `openpages.process-log.list`
- `openpages.log-collector.delete-log`   An event is generated when a Log Collector log file is deleted from the **Other> Logs** UI.
- `openpages.trace-options.list`
- `openpages.trace-options.update`   An event is generated when the trace logging settings are updated in the **Other > Logs > System tracing options** UI.
- `openpages.process.get`
- `openpages.process.list`

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

- `openpages.role.assign`   An event is generated when a role template is assigned to a user or group.
- `openpages.role.revoke`   An event is generated when a role template is removed from a user or group.
- `openpages.role-template.get`
- `openpages.role-template.list`
- `openpages.role-template.delete`   An event is generated when a role template is deleted.
- `openpages.role-template.disable`   An event is generated when a role template is disabled.
- `openpages.role-template.enable`   An event is generated when a role template is enabled.
- `openpages.role-template.create`   An event is generated when a role template is created.
- `openpages.role-template.lock`   An event is generated when a role template is locked.
- `openpages.role-template.unlock`   An event is generated when a role template is unlocked.
- `openpages.role-template.update`   An event is generated when the properties of a role template, such as its Name and Description, are updated.
- `openpages.role-template-access.add`   An event is generated when an object type is added to a role template.
- `openpages.role-template-access.update`   An event is generated when the access controls for object type are changed for a role template.
- `openpages.role-template-access.delete`   An event is generated when an object type is removed from a role template.
- `openpages.role-template-app-permission.update`   An event is generated when the application permissions that are assigned to a role template are changed.

Security rules:

- `openpages.security-rule.list`
- `openpages.security-rule.get`
- `openpages.record-level-security-rule.validate`   An event is generated when a record level security rule is validated.
- `openpages.record-level-security-rule.create`   An event is generated when a record level security rule is created.
- `openpages.record-level-security-rule.update`   An event is generated when a record level security rule is modified.
- `openpages.record-level-security-rule.enable`   An event is generated when a record level security rule is enabled.
- `openpages.record-level-security-rule.delete`   An event is generated when a record level security rule is deleted.
- `openpages.field-level-security-rule.validate`   An event is generated when a field level security rule is validated.
- `openpages.field-level-security-rule.create`   An event is generated when a field level security rule is created.
- `openpages.field-level-security-rule.update`   An event is generated when a field level security rule is modified.
- `openpages.field-level-security-rule.enable`   An event is generated when a field level security rule is enabled.
- `openpages.field-level-security-rule.delete`   An event is generated when a field level security rule is deleted.

Settings:

- `openpages.setting.get`
- `openpages.setting.update`   An event is generated when the value of a setting is modified.
- `openpages.setting.create`
- `openpages.settiing.list`
- `openpages.setting.add-folder`   An event is generated when a custom folder is created on the Settings page.
- `openpages.setting.copy`
- `openpages.setting.delete`
- `openpages.setting.list`

System admin mode:

- `openpages.system-admin-mode.enable`   An event is generated when System Admin Mode is enabled.
- `openpages.system-admin-mode.disable`   An event is generated when System Admin Mode is disabled.

System files:

- `openpages.page-and-template.list`
- `openpages.system-file-resource.list`
- `openpages.system-file-resource.copy`
- `openpages.system-file-resource.move`
- `openpages.system-file-resource.delete`
- `openpages.system-file-resource.rename`
- `openpages.system-file-resource.get`
- `openpages.system-file-resource.create`
- `openpages.system-file-resource.update`
- `openpages.system-file-resource-access.list`
- `openpages.system-file-resource-access.update`
- `openpages.system-file-resource-access.delete`

## Object types, profiles, schema, object instances events
{: #object-types}

Field dependencies:

- `openpages.field-dependency.list`
- `openpages.field-dependency.create`   An event is generated when a field dependency is created.
- `openpages.field-dependency.update`   An event is generated when a field dependency is modified.
- `openpages.field-dependency.enable`   An event is generated when a field dependency is enabled.
- `openpages.field-dependency.delete`   An event is generated when a field dependency is deleted.

Field groups, fields, and schema:

- `openpages.solution.get`
- `openpages.field-group.list`
- `openpages.field-group.create`   An event is generated when a field group is created.
- `openpages.field-group.update`   An event is generated when a field group is modified.
- `openpages.field-group.delete`
- `openpages.field-group.add`   An event is generated when a field group is added to an object type.
- `openpages.field-group.remove`   An event is generated when a field group is removed from an object type.
- `openpages.field.list`
- `openpages.field.create`   An event is generated when a field is created.
- `openpages.field.update`   An event is generated when a field is modified.
- `openpages.filters.list`
- `openpages.solution-profile.list`
- `openpages.object-type.list`
- `openpages.object-type.update`   An event is generated when the properties of an object type are modified.

Filters:

- `openpages.object-filter.list`
- `openpages.object-filter.get`
- `openpages.object-filter.create`   An event is generated when a public filter is defined for an object type.
- `openpages.object-filter.delete`   An event is generated when a public filter is deleted.

Profiles:

- `openpages.profile.list`
- `openpages.profile.get`
- `openpages.profile.update`   An event is generated when a profile is modified.
- `openpages.profile.create`   An event is generated when a profile is created.
- `openpages.profile.enable`   An event is generated when a profile is enabled.
- `openpages.profile.delete`   An event is generated when a profile is deleted.
- `openpages.profile-object-type.list`
- `openpages.profile-object-type.delete`   An event is generated when an object type is removed from a profile
- `openpages.profile-object-type.add`   An event is generated when an object type is added to a profile.
- `openpages.profile-actor.list`
- `openpages.profile.remove`
- `openpages.profile.add`
- `openpages.profile-report.delete`
- `openpages.profile-report.add`
- `openpages.profile-report.enable`
- `openpages.profile-object-type.get`
- `openpages.profile-object-field.list`
- `openpages.profile-object-field.delete`   An event is generated when an field is removed from a profile.
- `openpages.profile-object-field.add`   An event is generated when an field is added to a profile.
- `openpages.profile-object-field.update`
- `openpages.profile-object-filter.delete`   An event is generated when a public filter is removed from a profile.
- `openpages.profile-object-filter.add`   An event is generated when a public filter is added to a profile.

Objects:

- `openpages.resource.get`
- `openpages.file-resource-version.list`
- `openpages.resource.update`   An event is generated when an object instance is modified.
- `openpages.resource.bulk-update`   An event is generated when object instances are updated by a bulk operation.
- `openpages.file-resource.update`
- `openpages.resource.create`
- `openpages.file-resource.create`
- `openpages.resource.delete`   An event is generated when an object instance is deleted.
- `openpages.resource.lock`   An event is generated when an object instance is locked.
- `openpages.resource.unlock`   An event is generated when an object instance is unlocked.
- `openpages.resource.search`
- `openpages.resource.move`   An event is generated when an object instance is moved.
- `openpages.resource.list`
- `openpages.resource.export`

Object resets:

- `openpages.object-reset.get`
- `openpages.object-reset.list`
- `openpages.object-reset.start`

Object type associations:

- `openpages.object-relationship.list`
- `openpages.resource.add`
- `openpages.resource.remove-all`
- `openpages.resource.remove`
- `openpages.resource.copy`
- `openpages.resource-primary-parent.reassign`
- `openpages.object-relationship.enable`
- `openpages.object-relationship.update`

Recursive object types:

- `openpages.recursive-object-level.list`
- `openpages.recursive-object-level.create`
- `openpages.recursive-object-level.delete`

Solutions:

- `openpages.solution.list`
- `openpages.solution.create`
- `openpages.solution.update`
- `openpages.solution.delete`
- `openpages.field-exclusion.list`
- `openpages.field-exclusion.create`
- `openpages.field-exclusion.update`
- `openpages.field-exclusion.delete`

## Calculations, workflows, views, and other user interface events
{: #calc-workflow}

Calculations:

- `openpages.calculation.list`
- `openpages.calculation.get`
- `openpages.calculation.create`
- `openpages.calculation.update`
- `openpages.calculation.publish`
- `openpages.calculation.discard-draft`
- `openpages.calculation.delete`
- `openpages.calculation.enable`
- `openpages.bulk-calculation.start`

Dashboards:


- `openpages.admin-dashboard.list`
- `openpages.admin-dashboard.create`   An event is generated when a dashboard is created by using the **Solution Configuration > Dashboards** UI.
- `openpages.admin-dashboard.get`
- `openpages.admin-dashboard.update`   An event is generated when a dashboard is modified by using the **Solution Configuration > Dashboards** UI.
- `openpages.admin-dashboard.publish`   An event is generated when a dashboard is published by using the **Solution Configuration > Dashboards** UI.
- `openpages.admin-dashboard.discard-draft`   An event is generated when the unsaved changes to a dashboard in the **Solution Configuration > Dashboards** UI are discarded.
- `openpages.admin-dashboard.delete`   An event is generated when a dashboard is deleted by using the **Solution Configuration > Dashboards** UI.
- `openpages.admin-dashboard.enable`   An event is generated when a dashboard is set to **Active** by using the **Solution Configuration > Dashboards** UI.
- `openpages.user-dashboard.load`   An event is generated when a user Dashboard is accessed.
- `openpages.user-dashboard.update`   An event is generated when a user updates the Dashboard, for example by adding or modifying panels.


FastMap:

- `openpages.fastmap.validate`   An event is generated when an import file is validated by FastMap.
- `openpages.fastmap.import`   An event is generated when a FastMap import is started.

File attachments:

- `openpages.file-resource.download`
- `openpages.file-resource.checkout`
- `openpages.file-resource.checkin`
- `openpages.file-resource.cancel-checkout`
- `openpages.file-type.create`
- `openpages.file-type.disable`
- `openpages.file-type.enable`

<!-- - `openpages.file-type.enable-search`-->
<!--
Global search:
{: #global-search}
- `openpages.search-config.list`
- `openpages.search-config.update`-->

Folders:

- `openpages.folder-resource.create`
- `openpages.folder-resource.delete`

Net Promoter Score \(NPS\):

- `openpages.nps-settings.get`
- `openpages.nps-settings.update`   An event is generated when the settings for Net Promoter Score (NPS) are updated.

Questionnaires:

- `openpages.questionnaire-template.get`
- `openpages.questionnaire-template.add-default-objects`
- `openpages.questionnaire-template.copy-from-existing`
- `openpages.questionnaire-template.update`
- `openpages.questionnaire.copy-answers`
- `openpages.questionnaire-template.reorder`
- `openpages.questionnaire.upload-attachment`
- `openpages.questionnaire.get`

Rules \(Regulatory Event rules\):

- `openpages.rule.get`
- `openpages.rule.create`   An event is generated when a rule is created in the **Regulatory Event Rules** UI.
- `openpages.rule.update`   An event is generated when a rule in the **Regulatory Event Rules** UI is modified.
- `openpages.rule.delete`   An event is generated when a rule in the **Regulatory Event Rules** UI is deleted.
- `openpages.rule.enable`   An event is generated when a rule in the **Regulatory Event Rules** UI is enabled.
- `openpages.rule.list`

Scheduler jobs:

- `openpages.scheduler-job.get`
- `openpages.scheduler-job-log.list`   An event is generated when a job execution log is viewed.
- `openpages.scheduler-job.list`
- `openpages.scheduled-job.create`
- `openpages.scheduled-job.update`  An event is generated when a job definition is updated.
- `openpages.scheduled-job.enable`  An event is generated when a job is deleted.
- `openpages.scheduled-job.start`   An event is generated when a job starts.
- `openpages.scheduled-job.delete`   An event is generated when a job is deleted.

Tags:

- `openpages.tag.list`
- `openpages.tag.create`  An event is generated when a tag is created.
- `openpages.tag.update`  An event is generated when the properties of a tag are modified.
- `openpages.tag.enable`  An event is generated when a tag is enabled.
- `openpages.tag-association.get`
- `openpages.tag-association.add`  An event is generated when an object type is added to the list of enabled object types for tags.
- `openpages.tag-association.delete`  An event is generated when an object type is removed from the list of enabled object types for tags.
- `openpages.tag-association.update`

Themes:

- `openpages.theme.list`
- `openpages.theme.create`  An event is generated when a theme is created.
- `openpages.theme.get`
- `openpages.theme.update`  An event is generated when a theme is updated.
- `openpages.theme.delete`  An event is generated when a theme is deleted.
- `openpages.theme.enable`  An event is generated when a theme is enabled.

Workflows:

- `openpages.workflow.get`
- `openpages.workflow.create`
- `openpages.workflow.update`
- `openpages.workflow.publish`
- `openpages.workflow.delete`
- `openpages.workflow.enable`
- `openpages.workflow.list`
- `openpages.workflow.discard-draft`
- `openpages.workflow-resorce.synchronize`
- `openpages.workflow-resource.list`
- `openpages.workflow-resource.terminate`
- `openpages.workflow-resource.validate-action`
- `openpages.workflow-resource.bulk-start`
- `openpages.resource-workflow-action.bulk-run`
- `openpages.resource-workflow-action.run`
- `openpages.resource-workflow.start`

Views:

- `openpages.view.list`
- `openpages.view.get`
- `openpages.view.create`  An event is generated when a view is created.
- `openpages.view.update`  An event is generated when a view is modified.
- `openpages.view.validate`
- `openpages.view.publish`  An event is generated when a view is published.
- `openpages.view.delete`  An event is generated when a view is deleted.
- `openpages.view.discard-draft`  An event is generated when the unsaved changes to a view are discarded.
- `openpages.view.enable`  An event is generated when a view is enabled.
- `openpages.admin-view.create`  An event is generated when an admin view is created.

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

- `openpages.ai-model-configuration.list`
- `openpages.ai-model-configuration.get`
- `openpages.ai-model-configuration.create`
- `openpages.ai-model-configuration.update`
- `openpages.ai-model-configuration.delete`
- `openpages.ai-model-configuration.validate`
- `openpages.ai-model.suggest-insight`

<!--
Cognos:

- `openpages.cognos.enable`
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

- `openpages.watson-classifier.create`
- `openpages.watson-classifier.update`
- `openpages.watson-classifier.delete`
- `openpages.watson-classifier.validate`

Microsoft Office:
- `openpages.msoffice-resource.edit`
- `openpages.msoffice-resource.save`

watsonx Assistant:

- `openpages.watson-assistant.get`
- `openpages.watson-assistant.validate`
- `openpages.watson-assistant.configure`

Watson Language Translator:

- `openpages.watson-translator.get`
- `openpages.watson-translator.update`
- `openpages.watson-translator.validate`
- `openpages.watson-translator.translate`
- `openpages.watson-translator.translate-object`
- `openpages.watson-translator.translate-view`

## Feed provider events
{: #feeds}

Reg-Track:

- `openpages.reg-track.import`
- `openpages.reg-track.get`
- `openpages.reg-track.update`

Thomson Reuters:

- `openpages.taxonomy-mapping.download`
- `openpages.taxonomy-mapping.update`
- `openpages.trri.import`
- `openpages.trri.get`
- `openpages.trri.update`

Wolters Kluwer:

- `openpages.wk.import`
- `openpages.wk.get`
- `openpages.wk.update`

## API events
{: #api-events}

- `openpages.application-text.get`
- `openpages.application-text.list`
- `openpages.app-permission.get`
- `openpages.app-permission.list`
- `openpages.base-currency.get`  Get the base currency of an instance.
- `openpages.configuration.decrypt`
- `openpages.configuration.encrypt`
- `openpages.currency.get`
- `openpages.currency.list`   Get a list of currencies.
- `openpages.currency.update`
- `openpages.exchange-rate.bulk-update`  Update currencies in bulk.
- `openpages.exchange-rate.list`   Get a list of exchange rates.
- `openpages.exchange-rate.update`
- `openpages.file-resource.get`
- `openpages.file-resource.update`
- `openpages.folder.create`
- `openpages.folder.get`
- `openpages.folder.list`
- `openpages.folder.update`
- `openpages.folder-permission.get`
- `openpages.folder-template.get`
- `openpages.group.add`
- `openpages.group.get`
- `openpages.group.list`
- `openpages.group.update`
- `openpages.group-member.add`
- `openpages.group-member.delete`
- `openpages.group-member.list`
- `openpages.group-permission.list`
- `openpages.group-role-assignment.add`
- `openpages.group-role-assignment.delete`
- `openpages.group-role-assignment.list`
- `openpages.object-manager.fetch-dump`
- `openpages.object-manager.get-load-log`
- `openpages.object-manager.get-validate-log`
- `openpages.object-manager.submit-dump`
- `openpages.object-manager.submit-load`
- `openpages.object-manager.submit-validate`
- `openpages.object-manager.upload-load-data`
- `openpages.object-manager.upload-validate-data`
- `openpages.object-type.get`
- `openpages.object-type.list`
- `openpages.object-type-association.get`
- `openpages.object-type-association.list`
- `openpages.process.get`
- `openpages.process.list`
- `openpages.process.terminate`
- `openpages.process-log.list`
- `openpages.process-type.list`
- `openpages.profile.get`
- `openpages.profile.list`
- `openpages.profile-object-field.list`
- `openpages.query.execute`
- `openpages.questionnaire.get`
- `openpages.resource.add`
- `openpages.resource.associate`
- `openpages.resource.copy`
- `openpages.resource.delete`
- `openpages.resource.get`
- `openpages.resource.list`
- `openpages.resource.lock`
- `openpages.resource.move`
- `openpages.resource.unlock`
- `openpages.resource.unlock-descendants`
- `openpages.resource.update`
- `openpages.resource-activity.list`
- `openpages.resource-association.delete`
- `openpages.resource-association.get`
- `openpages.resource-association.list`
- `openpages.resource-permission.get`
- `openpages.resource-template.get`
- `openpages.role-template.get`
- `openpages.role-template.list`
- `openpages.role-template-access.list`
- `openpages.role-template-app-permission.list`
- `openpages.root-folder.get`
- `openpages.setting.get`
- `openpages.setting.list`
- `openpages.sub-group.add`
- `openpages.sub-group.delete`
- `openpages.sub-group.list`
- `openpages.system-admin-mode.get`
- `openpages.system-admin-mode.update`
- `openpages.tag.add`
- `openpages.tag.get`
- `openpages.tag.list`
- `openpages.tag.update`
- `openpages.tag-association.add`
- `openpages.tag-association.delete`
- `openpages.tag-association.list`
- `openpages.trace-options.update`
- `openpages.user.add`
- `openpages.user.anonymize`
- `openpages.user.get`
- `openpages.user.update`
- `openpages.user-app-permission.list`
- `openpages.user-impersonate.list`
- `openpages.user-membership.list`
- `openpages.user-password.reset`
- `openpages.user-role-assignment.add`
- `openpages.user-role-assignment.delete`
- `openpages.user-role-assignment.list`

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

## Analyzing events
{: #at_events_iam_analyze}

List events in your service that add additional information in requestData and responseData.

<!-- Provide information about the events in your service that add additional information in requestData and responseData. See the IAM Events topic for a sample topic that includes this section: /docs/activity-tracker?topic=activity-tracker-at_events_iam#at_events_iam_analyze.  -->
