# Export / import Advanced Pack entities

## Report

**Export**

```
bin/command export-import export --format=json --path="build/ExportImport" --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --skip-customization --skip-related-entities
```

**Import**

```
bin/command export-import import --format=json --path="build/ExportImport" --import-type=createAndUpdate --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --skip-customization --skip-related-entities
```

### Custom entities and fields export / import for Reports

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
bin/command export-import export --format=json --path="build/ExportImport" --import-type=createAndUpdate --entity-list="Report, ReportCategory, ReportFilter, ReportPanel" --skip-config --all-customization --skip-related-entities
```
