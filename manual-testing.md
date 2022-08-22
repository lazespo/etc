# Manual testing map

## Entities

### Account

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Contact

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Lead

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate
- [X] Lead Convert

### Opportunity

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Case

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Email Template

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Email Filter

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Email Folder

- [X] Creating
- [X] Updating
- [ ] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Personal Email Account

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Group Email Account

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Target List

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate
- [X] Populate the target list with leads using 'select all results'.

### Calendar

- [X] Create events.
- [X] A shared view.
- [X] Timeline.

### Meeting

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate
- [X] Send invitations
- [X] Popup reminder.
- [X] Email reminder.

### Call

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Task

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Campaign

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Knowledge Base

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Document

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate
- [X] Creating by drag-n-drpping file on the list view

### User

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

### Team

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate
- [X] Assign a team position to a user (Position List field).

### PDF Template

- [X] Creating
- [X] Updating
- [X] Remove from List View
- [X] Remove from Detail View
- [X] Duplicate

## Features

### Personal Email Account

- [X] Create account with IMAP and SMTP.
- [X] Check emails are received and available in the user's INBOX.
- [X] Test email sending from the account.

### Group Email Account

- [X] Create account with IMAP and SMTP.
- [X] Check emails are received.
- [X] Test email sending from the account.
- [X] Email-to-Case.

### Email

- [X] Apply email template, test placeholders
- [X] Save draft and send
- [X] Remove email

### Stream

- [X] Post on record
- [X] Post attachments
- [X] Update post
- [X] Remove post
- [X] Post to another user
- [X] Post to team

### Portal

- [X] Create a portal, with portal role, portal user, layout set
- [X] Check whether ACL is applied for the portal user 
- [X] Check whether layout set is applied for a logged portal user

### 2-factor authentication

- [X] Set up TOTP 2FA for a user and login under that user

### Passwords

- [X] An admin creates a user (with an email address non-empty), password is empty, *Send Email with Access Info to User* is checked. Check a received access email. Try to login under the new user.
- [X] An admin changes a password to another user (on the User edit view). 
- [X] An admin changes a password to another user with *Send Email with Access Info to User* checked (the user should have email address). Check a received email.
- [X] A regular user changes own password (from the dropdown on the User detail view).
- [X] Send password change link for another regular user (under the admin from the dropdown on the User detail view).
- [X] Send password change link for a portal user.
- [X] Forgot password from the login page. Recover access for a user.

### Import

- [X] Import CSV with email address, phone number.
- [X] Import Create Only.
- [X] Import Create and Update.
- [X] Check duplicate detection.
- [X] Import invalid email, check the record is available in the Errors panel.
- [X] Import in idle.
- [ ] Import by command line (manully).
- [X] Import with same params.
- [X] Revert import.

### Currency

- [X] Currency converting

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

- [X] Send mass email
- [ ] Tracking URL in mass email

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

- [ ] Creating
- [ ] Updating
- [ ] Remove
- [ ] Duplicate
- [ ] List type report
- [ ] Grid type report grouped by 1 field
- [ ] Grid type report grouped by 2 fields
- [ ] Grid type report grouped by 0 fields
- [ ] Grid type report with non-aggragate fields
- [ ] Report dashlet Grid
- [ ] Report dashlet List
- [ ] Report Panel
- [ ] Report Filter
- [ ] Send report in Email (from UI)

### Workflow

- [ ] Creating
- [ ] Updating
- [ ] Remove
- [ ] Duplicate

### BPM

- [ ] Creating
- [ ] Updating
- [ ] Remove
- [ ] Duplicate
- [ ] Run BPM process from record detail view

## Sales Pack

### Quote

- [ ] Creating
- [ ] Updating
- [ ] Remove
- [ ] Duplicate
- [ ] Print to PDF
- [ ] Send PDF in email

### Sales Order

- [ ] Creating
- [ ] Updating
- [ ] Remove
- [ ] Duplicate

### Invoice

- [ ] Creating
- [ ] Updating
- [ ] Remove
- [ ] Duplicate

### Product

- [ ] Creating
- [ ] Updating
- [ ] Remove
- [ ] Duplicate

## Google integration

### Google Calendar

- [ ] Create Meeting, Call on Espo side
- [ ] Check sync. on Google side
- [ ] Create Meeting, Call on Google side
- [ ] Check sync. on Espo side
- [ ] Edit Meeting, on Espo side
- [ ] Check changes on Google side
- [ ] Edit Meeting, on Google side
- [ ] Check changes on Espo side

### Google Contacts

- [ ] Push contacts to Google
- [ ] Check contacts availability on Google side

### Gmail secure authentication

- [ ] Check Personal Email Account auth
- [ ] Check Group Email Account auth
- [ ] Check fetch emails on Espo side
- [ ] Sending emails from Espo

### Google Maps

- [ ] Check whether Google Map can be printed in PDF

## Outlook Integration

### Outlook Calendar

- [ ] Create one Meeting/Call with an arbitrary date for the next 7-8 months on Espo side
- [ ] Check sync. on Outlook side
- [ ] Create one Meeting/Call with an arbitrary date for the next 7-8 months on Outlook side
- [ ] Check sync. on Espo side
- [ ] Edit Meeting, on Espo side
- [ ] Check changes on Outlook side
- [ ] Edit Meeting, on Outlook side
- [ ] Check changes on Espo side

### Outlook Contacts

- [ ] Push contacts to Outlook
- [ ] Check contacts availability on Outlook side

### Outlook emails

- [ ] Check fetch emails on Espo side (Personal Email Account)
- [ ] Check fetch emails on Espo side (Group Email Account)
- [ ] Sending emails from Espo

## VoIP Integration

### Asterisk AMI

- [ ] Make a call from sip "201" to sip "202"
- [ ] Pick up the phone
- [ ] Create a Contact from a call
- [ ] Make a click-to-call from created Contact
- [ ] Pick up the phone on sip "201"
- [ ] Pick up the phone on sip "202"

### Twilio

- [ ] Make a call from sip "201" to sip "202"
- [ ] Pick up the phone
- [ ] Create a Contact from a call
- [ ] Make a click-to-call from created Contact
- [ ] Pick up the phone on sip "201"
- [ ] Pick up the phone on sip "202"

### Starface

- [ ] Make a call from sip "10" to sip "11"
- [ ] Pick up the phone
- [ ] Create a Contact from a call
- [ ] Make a click-to-call from created Contact
- [ ] Pick up the phone on sip "10"
- [ ] Pick up the phone on sip "11"

## Mailchimp Integration

- [ ] Create a Campaign and Target List for MailChimp
- [ ] Sync Target List with EspoCRM into MailChimp
- [ ] Configure bulk email Campaign into MailChimp
- [ ] Start bulk email Campaign
- [ ] Check recieved emails

## Real Estate

- [ ] Test properties and requests matching

## Demo Data

- [ ] Intstall
- [ ] Remove
