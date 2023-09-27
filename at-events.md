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

The following table lists the actions in the Console that generate an event:

| Action                                   | Description |
|------------------------------------------|---------|
| `openpages.services.list`                  | An event is generated when |
| `openpages.services-filter.list`           | An event is generated when |
| `openpages.services.get`                   | An event is generated when |
| `openpages.services-configure.update`      | An event is generated when |
| `openpages.services-eventnotification.update`| An event is generated when |
| `openpages.services-transfer-host.update`  | An event is generated when you transfer a custom host name to another instance. |
| `openpages.services-configure-host.update` | An event is generated when |
| `openpages.services.update`                | An event is generated when |
| `openpages.services.delete`                | An event is generated when |
| `openpages.services.upgrade`               | An event is generated when |
| `openpages.service-allow-list.update`       | An event is generated when the allow list is updated. |
| `openpages.service-cpu-metrics.get`       | An event is generated when |
| `openpages.service-user-metrics.get`      | An event is generated when |
| `openpages.service-storage-metrics.get`   | An event is generated when |
| `openpages.service-custom-resource.update`      | An event is generated when |
| `openpages.services-sol-usage.update`      | An event is generated when |
| `openpages.services.add`                   | An event is generated when you add an instance. |
| `openpages.services.update`                | An event is generated when |
| `openpages.services.delete`                | An event is generated when |
| `openpages.services-status.enabled`       | An event is generated when |
| `openpages.services-promoted-component-version.get`  | An event is generated when |
{: caption="Table 1. Actions that generate platform events (UI)" caption-side="bottom"}


## Users, groups, login, and logout events
{: #users-groups}

Login, Logout, Session, Authentication:

- `openpages.user.logoff`
- `openpages.user.logon`
- `openpages.user.session-expire`

User Management:

- `openpages.user.get`
- `openpages.user.list`
- `openpages.user.create`
- `openpages.user.update`
- `openpages.user.enable`
- `openpages.user.disable`
- `openpages.user.lock`
- `openpages.user.unlock`
- `openpages.user-locale.update`
- `openpages.user-current-profile.update`
- `openpages.user-reporting-period.update`
- `openpages.user-password.update`
- `openpages.user-preference.set`
- `openpages.user-association.add`
- `openpages.user-association.delete`
- `openpages.user-association.update`

Group Management:

- `openpages.group.list`
- `openpages.group.create`
- `openpages.group.update`
- `openpages.group.get`
- `openpages.group-administrator-permission.revoke`
- `openpages.group-administrator-permission.assign`
- `openpages.group-administrator-permission.update`
- `openpages.group-membership.add`
- `openpages.group-membership.remove`
- `openpages.group-permission.update`

## System administration and security events
{: #system-admin}

Audit trail:

- `openpages.resource-activity.list`
- `openpages.resource-activity.get`

Currencies:

- `openpages.currency.list`
- `openpages.currency.update`
- `openpages.currency.enable`
- `openpages.currency.disable`
- `openpages.currency-history.list`
- `openpages.currency.upload`

Encryption keystore:

- `openpages.encryption-keystore.get`
- `openpages.encryption-keystore.enable`
- `openpages.encryption-keystore.update`

Environment migration:

- `openpages.configuration.list-import`
- `openpages.configuration.submit-import`
- `openpages.configuration.validate-import`
- `openpages.configuration.list-export`
- `openpages.configuration.get`
- `openpages.configuration.submit-export`

Localization \(object text and application text\):

- `openpages.object-text.list`
- `openpages.object-text.update`
- `openpages.application-text.update`
- `openpages.application-text-key.list`
- `openpages.object-text-key.list`
- `openpages.application-text.list`

Logs, processes, trace logs:

- `openpages.log-collector.launch`
- `openpages.log-collector.download-log`

<!--
- `openpages.cognos-reporting-framework.list`
- `openpages.cognos-reporting-framework.generate`-->
- `openpages.process-log.list`
- `openpages.log-collector.delete-log`
- `openpages.trace-options.list`
- `openpages.trace-options.update`
- `openpages.process.get`
- `openpages.process.list`

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

- `openpages.role.assign`
- `openpages.role.revoke`
- `openpages.role-template.get`
- `openpages.role-template.list`
- `openpages.role-template.delete`
- `openpages.role-template.disable`
- `openpages.role-template.enable`
- `openpages.role-template.create`
- `openpages.role-template.lock`
- `openpages.role-template.unlock`
- `openpages.role-template.update`
- `openpages.role-template-access.add`
- `openpages.role-template-access.update`
- `openpages.role-template-access.delete`
- `openpages.role-template-app-permission.update`

Security rules:

- `openpages.security-rule.list`
- `openpages.security-rule.get`
- `openpages.record-level-security-rule.validate`
- `openpages.record-level-security-rule.create`
- `openpages.record-level-security-rule.update`
- `openpages.record-level-security-rule.enable`
- `openpages.record-level-security-rule.delete`
- `openpages.field-level-security-rule.validate`
- `openpages.field-level-security-rule.create`
- `openpages.field-level-security-rule.update`
- `openpages.field-level-security-rule.enable`
- `openpages.field-level-security-rule.delete`

Settings:

- `openpages.setting.get`
- `openpages.setting.update`
- `openpages.setting.create`
- `openpages.settiing.list`
- `openpages.setting.add-folder`
- `openpages.setting.copy`
- `openpages.setting.delete`
- `openpages.setting.list`

System admin mode:

- `openpages.system-admin-mode.enable`
- `openpages.system-admin-mode.disable`

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

- `openpages.user-dashboard.update`
- `openpages.field-dependency.list`
- `openpages.field-dependency.create`
- `openpages.field-dependency.update`
- `openpages.field-dependency.enable`
- `openpages.field-dependency.delete`

Field groups, fields, and schema:

- `openpages.solution.get`
- `openpages.field-group.list`
- `openpages.field-group.create`
- `openpages.field-group.update`
- `openpages.field-group.delete`
- `openpages.field-group.add`
- `openpages.field-group.remove`
- `openpages.field.list`
- `openpages.field.create`
- `openpages.field.update`
- `openpages.filters.list`
- `openpages.solution-profile.list`
- `openpages.object-type.list`
- `openpages.object-type.update`

Filters:

- `openpages.object-filter.list`
- `openpages.object-filter.get`
- `openpages.object-filter.create`
- `openpages.object-filter.delete`

Profiles:

- `openpages.profile.list`
- `openpages.profile.get`
- `openpages.profile.update`
- `openpages.profile.create`
- `openpages.profile.enable`
- `openpages.profile.delete`
- `openpages.profile-object-type.list`
- `openpages.profile-object-type.delete`
- `openpages.profile-object-type.add`
- `openpages.profile-actor.list`
- `openpages.profile.remove`
- `openpages.profile.add`
- `openpages.profile-report.delete`
- `openpages.profile-report.add`
- `openpages.profile-report.enable`
- `openpages.profile-object-type.get`
- `openpages.profile-object-field.list`
- `openpages.profile-object-field.delete`
- `openpages.profile-object-field.add`
- `openpages.profile-object-field.update`
- `openpages.profile-object-filter.delete`
- `openpages.profile-object-filter.add`

Objects:

- `openpages.resource.get`
- `openpages.file-resource-version.list`
- `openpages.resource.update`
- `openpages.resource.bulk-update`
- `openpages.file-resource.update`
- `openpages.resource.create`
- `openpages.file-resource.create`
- `openpages.resource.delete`
- `openpages.resource.lock`
- `openpages.resource.unlock`
- `openpages.resource.search`
- `openpages.resource.move`
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
- `openpages.admin-dashboard.create`
- `openpages.admin-dashboard.get`
- `openpages.admin-dashboard.update`
- `openpages.admin-dashboard.publish`
- `openpages.admin-dashboard.discard-draft`
- `openpages.admin-dashboard.delete`
- `openpages.admin-dashboard.enable`
- `openpages.user-dashboard.load`
- `openpages.user-dashboard.update`

FastMap:

- `openpages.fastmap.validate`
- `openpages.fastmap.import`

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
- `openpages.nps-settings.update`

Questionnaires:

- `openpages.questionnaire-template.get`
- `openpages.questionnaire-template.add-default-objects`
- `openpages.questionnaire-template.copy-from-existing`
- `openpages.questionnaire-template.update`
- `openpages.questionnaire.copy-answers`
- `openpages.questionnaire-template.reorder`
- `openpages.questionnaire.upload-attachment`
- `openpages.questionnaire.get`

Rules \(Rules Engine\):

- `openpages.rule.get`
- `openpages.rule.create`
- `openpages.rule.update`
- `openpages.rule.delete`
- `openpages.rule.enable`
- `openpages.rule.list`

Scheduler jobs:

- `openpages.scheduler-job.get`
- `openpages.scheduler-job-log.list`
- `openpages.scheduler-job.list`
- `openpages.scheduled-job.create`
- `openpages.scheduled-job.update`
- `openpages.scheduled-job.enable`
- `openpages.scheduled-job.start`
- `openpages.scheduled-job.delete`

Tags:

- `openpages.tag.list`
- `openpages.tag.create`
- `openpages.tag.update`
- `openpages.tag.enable`
- `openpages.tag-association.get`
- `openpages.tag-association.add`
- `openpages.tag-association.delete`
- `openpages.tag-association.update`

Themes:

- `openpages.theme.list`
- `openpages.theme.create`
- `openpages.theme.get`
- `openpages.theme.update`
- `openpages.theme.delete`
- `openpages.theme.enable`

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
- `openpages.view.create`
- `openpages.view.update`
- `openpages.view.validate`
- `openpages.view.publish`
- `openpages.view.delete`
- `openpages.view.discard-draft`
- `openpages.view.enable`
- `openpages.admin-view.create`

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

Watson Assistant:

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
- `openpages.base-currency.get` <!--- `openpages.cognos.integrate`-->
- `openpages.configuration.decrypt`
- `openpages.configuration.encrypt`
- `openpages.currency.get`
- `openpages.currency.list`
- `openpages.currency.update`
- `openpages.current-reporting-period.get`
- `openpages.exchange-rate.bulk-update`
- `openpages.exchange-rate.list`
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
- `openpages.report-fragment.execute`
- `openpages.reporting-period.get`
- `openpages.reporting-period.list`
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
