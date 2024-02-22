# Export / import Advanced Pack entities

## Report

**Export**

```
bin/command export-import export --format=json --path="./data/export-import" --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="./data/export-import" --import-type=createAndUpdate
```

### Custom entities and fields

If the Target Entity of at least one of the reports is custom entity, you need to add it to the `--entity-list` option. Example:

**Export**

```
bin/command export-import export --format=json --path="./data/export-import" --entity-list="Report, ReportCategory, ReportFilter, ReportPanel, CustomEntity" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="./data/export-import" --import-type=createAndUpdate
```

If the Target Entities of the reports are default entities, but at least one field in the one report is a custom field, you should add an `--all-customization` option and remove `--skip-customization` option. Example:

**Export**

```
bin/command export-import export --format=json --path="./data/export-import" --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --all-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="./data/export-import" --import-type=createAndUpdate
```

## Workflow

**Export**

```
bin/command export-import export --format=json --path="./data/export-import" --entity-list="Workflow, WorkflowCategory, WorkflowCategoryPath" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="./data/export-import" --import-type=createAndUpdate
```

If the Target Entity of at least one of the workflows is custom entity, you need to add it to the `--entity-list` option. Example:

**Export**

```
bin/command export-import export --format=json --path="./data/export-import" --entity-list="Workflow, WorkflowCategory, WorkflowCategoryPath, CustomEntity" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="./data/export-import" --import-type=createAndUpdate
```

### Actions performance

If there are certain actions in the workflow, it is also important to add the following entities to the `--entity-list` option (depending on the workflow actions):

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
bin/command export-import export --format=json --path="./data/export-import" --entity-list="BpmnFlowchart" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="./data/export-import" --import-type=createAndUpdate
```

If the Target Entity of at least one of the BPMs is custom entity, you need to add it to the `--entity-list` option. Example:

**Export**

```
bin/command export-import export --format=json --path="./data/export-import" --entity-list="BpmnFlowchart, CustomEntity" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="./data/export-import" --import-type=createAndUpdate
```

Depending on the presence of certain BPM elements, the following entities should be added to the `--entity-list` option:

- Task - see [Actions performance for Workflow and BPMs](#actions-performance)
- Send Message Task - EmailTemplate, User, Team
- User Task - Team
