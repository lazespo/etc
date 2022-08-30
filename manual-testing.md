### Import

- [X] Import CSV with email address, phone number.
- [X] Import Create Only.
- [X] Import Create and Update.
- [X] Check duplicate detection.
- [X] Import invalid email, check the record is available in the Errors panel.
- [X] Import in idle.
- [X] Import by command line (manully).
- [X] Import with same params.
- [X] Revert import.

### Currency

- [X] Currency converting.

### Entity Manager

- [X] Create a custom entity.
- [X] Edit entity.
- [X] Edit formula.
- [X] Create custom field.
- [X] Edit custom field.
- [X] Delete custom field.
- [X] Delete custom entity.

### Layout sets

- [X] Create a layout set.
- [X] Apply the layout set to a team and test it's working for a logged user (the team should be a default team for the user).

### Lead Capture

- [X] Set up lead capture without opt-in confirmation, send API request, check lead is created.
- [X] Set up lead capture with opt-in confirmation, send API request, check whether works properly.
- [X] Check duplicate detecting works properly.

### Mass Email

- [X] Send mass email.
- [ ] Tracking URL in mass email.

## Configure WebSocket

1. Configure websocker service.
2. Enable websocket.
3. Test websocker funtionality.

## Test upgrading to the next version

The test package: https://github.com/tmachyshyn/espocrm-tips/raw/master/_static/files/testing/test-upgrade.zip

### 1. Prepare the upgrade package

1. Download and unzip.

2. Replace `7.1.0` to your current version in the `manifest.json`. The current version is the version of the next release, e.g. if you test a master of `7.2.0`, then it's `7.2.0`.

3. Pack the package with a new `manifest.json`.

### 2. Test UI upgrade

Go to Administration > Upgrade.

### 3. Test cli upgrade

```
bin/command upgrade --file="test-upgrade.zip"
```


## Advanced Pack

### Report

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] List type report.
- [ ] Grid type report grouped by 1 field.
- [ ] Grid type report grouped by 2 fields.
- [ ] Grid type report grouped by 0 fields.
- [ ] Grid type report with non-aggragate fields.
- [ ] Report dashlet Grid.
- [ ] Report dashlet List.
- [ ] Report Panel.
- [ ] Report Filter.
- [ ] Send report in Email (from UI).

### Workflow

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

### BPM

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Run BPM process from record detail view.

## Sales Pack

### Quote

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Printing to PDF.
- [ ] Sending PDF in email.

### Sales Order

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

### Invoice

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

### Product

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

## Google integration

### Google Calendar

- [ ] Create Meeting, Call on Espo side.
- [ ] Check sync. on Google side.
- [ ] Create Meeting, Call on Google side.
- [ ] Check sync. on Espo side.
- [ ] Edit Meeting, on Espo side.
- [ ] Check changes on Google side.
- [ ] Edit Meeting, on Google side.
- [ ] Check changes on Espo side.

### Google Contacts

- [ ] Push contacts to Google.
- [ ] Check contacts availability on Google side.

### Gmail secure authentication

- [ ] Check Personal Email Account auth.
- [ ] Check Group Email Account auth.
- [ ] Check fetch emails on Espo side.
- [ ] Sending emails from Espo.

### Google Maps

- [ ] Check whether Google Map can be printed in PDF.

## Outlook Integration

### Outlook Calendar

- [ ] Create one Meeting/Call with an arbitrary date for the next 7-8 months on Espo side.
- [ ] Check sync. on Outlook side.
- [ ] Create one Meeting/Call with an arbitrary date for the next 7-8 months on Outlook side.
- [ ] Check sync. on Espo side.
- [ ] Edit Meeting, on Espo side.
- [ ] Check changes on Outlook side.
- [ ] Edit Meeting, on Outlook side.
- [ ] Check changes on Espo side.

### Outlook Contacts

- [ ] Push contacts to Outlook.
- [ ] Check contacts availability on Outlook side.

### Outlook emails

- [ ] Check fetch emails on Espo side (Personal Email Account).
- [ ] Check fetch emails on Espo side (Group Email Account).
- [ ] Sending emails from Espo.

## VoIP Integration

### Asterisk AMI

- [ ] Make a call from sip "201" to sip "202".
- [ ] Pick up the phone.
- [ ] Create a Contact from a call.
- [ ] Make a click-to-call from created Contact.
- [ ] Pick up the phone on sip "201".
- [ ] Pick up the phone on sip "202".

### Twilio

- [ ] Make a call from sip "201" to sip "202".
- [ ] Pick up the phone.
- [ ] Create a Contact from a call.
- [ ] Make a click-to-call from created Contact.
- [ ] Pick up the phone on sip "201".
- [ ] Pick up the phone on sip "202".

### Starface

- [ ] Make a call from sip "10" to sip "11".
- [ ] Pick up the phone.
- [ ] Create a Contact from a call.
- [ ] Make a click-to-call from created Contact.
- [ ] Pick up the phone on sip "10".
- [ ] Pick up the phone on sip "11".

## Mailchimp Integration

- [ ] Create a Campaign and Target List for MailChimp.
- [ ] Sync Target List with EspoCRM into MailChimp.
- [ ] Configure bulk email Campaign into MailChimp.
- [ ] Start bulk email Campaign.
- [ ] Check recieved emails.

## Real Estate

- [ ] Test properties and requests matching.

## Demo Data

- [ ] Install.
- [ ] Remove.
