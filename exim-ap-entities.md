# Export / import Advanced Pack entities

* [Report](#report)
* [Workflow](#workflow)
* [BPM](#bpm)
* [Custom entities and fields export / import for Reports](#custom-entities-and-fields)
* [Actions performance for Workflow and BPMs](#actions-performance)

## Report

**Export**

```
bin/command export-import export --format=json --path="build/ExportImport" --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="build/ExportImport" --import-type=createAndUpdate --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --skip-customization --skip-related-entities
```

### Custom entities and fields

If the Target Entity of at least one of the reports is custom entity, you need to add it to the `--entity-list` option. Example:

**Export**

```
bin/command export-import export --format=json --path="build/ExportImport" --entity-list="Report, ReportCategory, ReportFilter, ReportPanel, CustomEntity" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="build/ExportImport" --import-type=createAndUpdate --entity-list="Report, ReportCategory, ReportFilter, ReportPanel, CustomEntity" --skip-config --skip-customization --skip-related-entities
```

If the Target Entities of the reports are default entities, but at least one field in the one report is a custom field, you should add an `--all-customization` option and remove `--skip-customization` option. Example:

**Export**

```
bin/command export-import export --format=json --path="build/ExportImport" --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --all-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="build/ExportImport" --import-type=createAndUpdate --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --all-customization --skip-related-entities
```

## Workflow

**Export**

```
bin/command export-import export --format=json --path="build/ExportImport" --entity-list="Workflow, WorkflowCategory, WorkflowCategoryPath" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="build/ExportImport" --import-type=createAndUpdate --entity-list="Workflow, WorkflowCategory, WorkflowCategoryPath" --skip-config --skip-customization --skip-related-entities
```

If the Target Entity is custom entity, it must be included in the `--entity-list` option.

### Actions performance

If there are certain actions in the Workflow, it is also important to add the following entities to the `--entity-list` option (depending on the Workflow actions):

- Send Email - EmailTemplate, User, Team
- Create Record - custom entity name if it is present in the action
- Create Related Record - custom entity name if it is present in the action
- Update Related Record - custom entity name if it is present in the action
- Link with another Record - custom entity name  if it is present in the action
- Unlink from another Record - custom entity name  if it is present in the action
- Apply Assignment Rule - Team, Report
- Create Notification - User, Team
- Make Followed - User, Team
- Start BPM Process - BpmnFlowchart

## BPM

**Export**

```
bin/command export-import export --format=json --path="build/ExportImport" --entity-list="BpmnFlowchart" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="build/ExportImport" --import-type=createAndUpdate --entity-list="BpmnFlowchart" --skip-config --skip-customization --skip-related-entities
```

If the Target Entity is custom entity, it must be included in the `--entity-list` option.

Depending on the presence of certain BPM elements, the following entities should be added to the `--entity-list` option:

- Task - see [Actions performance for Workflow and BPMs](#actions-performance)
- Send Message Task - EmailTemplate, User, Team
- User Task - Team
