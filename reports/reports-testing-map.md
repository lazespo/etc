# Manual Report Testing

When testing, be sure to keep the browser console open (F12) and open EspoCRM error logs. If there are errors, create a bug report in Asana.

## List Reports

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Report with ACL.
- [ ] Report without ACL.
- [ ] Complex Expression filter.
- [ ] Without Complex Expression filter (any other).
- [ ] Without filters.
- [ ] Report dashlet.
- [ ] Report Panel.
- [ ] Report Filter.
- [ ] Send in Email (from UI).
- [ ] Print to PDF.
- [ ] Export in CSV.
- [ ] Export in XLSX.
- [ ] Email Sending (scheduled).
- [ ] Scheduled Workflow.
- [ ] Manual sync with Target List.
- [ ] Scheduled sync with Target List.

## Grid Reports

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Complex Expression filter.
- [ ] Without Complex Expression filter (any other).
- [ ] Without filters.
- [ ] Grouped by 0 fields with ACL.
- [ ] Grouped by 0 fields without ACL.
- [ ] Grouped by 1 field with ACL.
- [ ] Grouped by 1 fields without ACL.
- [ ] Grouped by 2 fields with ACL.
- [ ] Grouped by 2 fields without ACL.
- [ ] Click in the report results on the fields by which it is grouped, check if everything is displayed correctly.
- [ ] With non-aggregate fields (non-grouping) with ACL.
- [ ] With non-aggregate fields (non-grouping) without ACL.
- [ ] With non-aggregate fields (grouping) with ACL.
- [ ] With non-aggregate fields (grouping) without ACL.
- [ ] Report dashlet.
- [ ] Report Panel.
- [ ] Report Filter.
- [ ] Send in Email (from UI).
- [ ] Print to PDF.
- [ ] Export in CSV.
- [ ] Export in XLSX.
- [ ] Email Sending (scheduled).

### Grouping By field types

- [ ] Attachment Multiple
- [ ] Auto-increment
- [ ] Barcode
- [ ] Boolean
- [ ] Currency
- [ ] Date
- [ ] Date-Time
- [ ] Enum
- [ ] File
- [ ] Float
- [ ] Image
- [ ] Integer
- [ ] Number
- [ ] Url
- [ ] Varchar
- [ ] Wysiwyg

## Joint Grid Reports

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Report dashlet.
- [ ] Send in Email (from UI).
- [ ] Print to PDF.
- [ ] Export in CSV.
- [ ] Export in XLSX.
- [ ] Email Sending (scheduled).

## Reports on Portal

### List Report
- [ ] Read.
- [ ] Report Dashlet.
- [ ] Report Panel.
- [ ] Report Filter.

### Grid Report
- [ ] Read.
- [ ] Report Dashlet.
- [ ] Report Panel.
- [ ] Report Filter.

---

**Reports, Report Panels, Report Filters import file:** https://github.com/lazespo/etc/blob/main/reports/ExportImport.zip

*Note*: create `birthOfDate` field with Date type for Contact entity (for Contacts that have birthday today report).
