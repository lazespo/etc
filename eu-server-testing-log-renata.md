# Manual testing map

## Administration

- [x] Change language.
- [x] Rebuild.

## Entities

### Account

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Contact

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Lead

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Lead Convert.

### Opportunity

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Create Document from Bottom Panel.
- [x] Select Document from Bottom Panel.

### Case

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Email Template

- [x] Creating.
- [x] Updating.
- [x] Remove from List View.
- [x] Remove from Detail View.
- [x] Duplicate.

### Email Filter

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Apply for imported emails (Personal Email).
- [x] Apply for imported emails (Group Email).

### Email Folder

- [x] Creating.
- [x] Updating.
- [x] Removing from Detail View.
- [x] Duplicating.

### Group Email Folder

- [x] Creating.
- [x] Updating.
- [x] Removing from Detail View.
- [x] Duplicating.

### Personal Email Account

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Group Email Account

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Target List

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Populate the target list with leads using 'select all results'.

### Calendar

- [x] Create events.
- [x] A shared view.
- [x] Timeline.

### Meeting

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Send invitations.
- [x] Popup reminder.
- [x] Email reminder.

### Call

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Task

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Campaign

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Knowledge Base

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Send in email.

### Document

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Creating by drag-n-drpping file on the list view.

### User

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

### Team

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Assign a team position to a user (Position List field).

### PDF Template

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

## Features

### Personal Email Account

- [x] Create account with IMAP and SMTP.
- [x] Check emails are received and available in the user's INBOX.
- [x] Test email sending from the account.

### Group Email Account

- [x] Create account with IMAP and SMTP.
- [x] Check emails are received.
- [x] Test email sending from the account.
- [x] Email-to-Case.

### Email

- [x] Apply email template, test placeholders.
- [x] Save draft and send.
- [x] Remove email.

### Stream

- [x] Post on record.
- [x] Post attachments.
- [x] Update post.
- [x] Remove post.
- [x] Post to another user.
- [x] Post to team.

### Portal

- [x] Create a portal, with portal role, portal user, layout set.
- [x] Check whether ACL is applied for the portal user.
- [x] Check whether layout set is applied for a logged portal user.

### 2-factor authentication

- [x] Set up TOTP 2FA for a user and login under that user.

### Passwords

- [x] An admin creates a user (with an email address non-empty), password is empty, *Send Email with Access Info to User* is checked. Check a received access email. Try to login under the new user.
- [x] An admin changes a password to another user (on the User edit view). 
- [x] An admin changes a password to another user with *Send Email with Access Info to User* checked (the user should have email address). Check a received email.
- [x] A regular user changes own password (from the dropdown on the User detail view).
- [x] Send password change link for another regular user (under the admin from the dropdown on the User detail view).
- [x] Send password change link for a portal user.
- [x] Forgot password from the login page. Recover access for a user.

### Import

- [x] Import CSV with email address, phone number.
- [x] Import Create Only.
- [x] Import Create and Update.
- [x] Check duplicate detection.
- [x] Import invalid email, check the record is available in the Errors panel.
- [x] Import in idle.
- [x] Import by command line (manully).
- [x] Import with same params.
- [x] Revert import.

### Currency

- [x] Currency converting.

### Entity Manager

- [x] Create a custom entity.
- [x] Edit entity.
- [x] Edit formula.
- [x] Create custom field.
- [x] Edit custom field.
- [x] Delete custom field.
- [x] Delete custom entity.

### Layout sets

- [x] Create a layout set.
- [x] Apply the layout set to a team and test it's working for a logged user (the team should be a default team for the user).

### Lead Capture

- [x] Set up lead capture without opt-in confirmation, send API request, check lead is created.
- [x] Set up lead capture with opt-in confirmation, send API request, check whether works properly.
- [x] Check duplicate detecting works properly.

### Mass Email

- [x] Send mass email.
- [x] Tracking URL in mass email.

## OIDC

- [ ] Create User.
- [ ] Change Username Claim.
- [ ] Allow OIDC login for admin users.
- [ ] Sync Teams.

## Advanced Pack

### Report

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] List type report.
- [x] Grid type report grouped by 1 field.
- [x] Grid type report grouped by 2 fields.
- [x] Grid type report grouped by 0 fields.
- [x] Grid type report with non-aggregate fields (non-grouping).
- [x] Grid type report with non-aggregate fields (grouping).
- [x] Report dashlet Grid.
- [x] Report dashlet List.
- [x] Report Panel.
- [x] Report Filter.
- [x] Send report in Email (from UI).
- [x] Print to PDF.

### Workflow

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating. 
- [x] Action "Send Email".

### BPM

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Run BPM process from record detail view.

## Sales Pack

### Quote

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Printing to PDF.
- [x] Sending PDF in email.

### Sales Order

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Printing to PDF.
- [x] Sending PDF in email.

### Invoice

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Printing to PDF.
- [x] Sending PDF in email.

### Product

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.

## Google Integration

### Google Calendar

- [x] Create Meeting, Call on Espo side.
- [x] Check sync. on Google side.
- [x] Create Meeting, Call on Google side.
- [x] Check sync. on Espo side.
- [x] Edit Meeting, on Espo side.
- [x] Check changes on Google side.
- [x] Edit Meeting, on Google side.
- [x] Check changes on Espo side.

### Google Contacts

- [x] Push contacts to Google.
- [x] Check contacts availability on Google side.

### Gmail secure authentication

- [x] Check Personal Email Account auth.
- [x] Check Group Email Account auth.
- [x] Check fetch emails on Espo side.
- [x] Sending emails from Espo.
- [x] IMAP connection with OAuth.
- [x] SMTP connection with OAuth.

### Google Maps

- [x] Check whether Google Map can be printed in PDF.

## Outlook Integration

### Outlook Calendar

- [x] Create one Meeting/Call on Espo side.
- [x] Check sync. on Outlook side.
- [x] Edit Meeting, on Espo side.
- [x] Check changes on Outlook side.
- [x] Create one Meeting/Call on Outlook side. 
- [x] Check sync. on Espo side.
- [x] Edit Meeting, on Outlook side.
- [x] Check changes on Espo side.
- [x] Create one Meeting/Call with an arbitrary date for the next 7-8 months on Espo side.
- [x] Check sync. on Outlook side.
- [x] Edit Meeting, on Espo side.
- [x] Check changes on Outlook side.
- [ ] Create one Meeting/Call with an arbitrary date for the next 7-8 months on Outlook side. - https://app.asana.com/0/932884031059353/1202920244817837
- [ ] Check sync. on Espo side.
- [ ] Edit Meeting, on Outlook side.
- [ ] Check changes on Espo side.

### Outlook Contacts

- [x] Push contacts to Outlook.
- [x] Check contacts availability on Outlook side.
- [x] Check Contacts folders in External Accounts settings. 

### Outlook emails

- [x] Check fetch emails on Espo side (Personal Email Account).
- [x] Check fetch emails on Espo side (Group Email Account).
- [x] Sending emails from Espo.
- [x] IMAP connection with OAuth.
- [x] SMTP connection with OAuth.

## VoIP Integration

### Asterisk AMI

- [ ] Make a call from sip "201" to sip "202".
- [ ] Pick up the phone.
- [ ] Create a Contact from a call.
- [ ] Make a click-to-call from created Contact.
- [ ] Pick up the phone on sip "201".
- [ ] Pick up the phone on sip "202".

### Twilio

- [x] Make a call from sip "201" to sip "202".
- [x] Pick up the phone.
- [x] Create a Contact from a call.
- [x] Make a click-to-call from created Contact.
- [x] Pick up the phone on sip "201".
- [x] Pick up the phone on sip "202".

### Starface

- [ ] Make a call from sip "10" to sip "11".
- [ ] Pick up the phone.
- [ ] Create a Contact from a call.
- [ ] Make a click-to-call from created Contact.
- [ ] Pick up the phone on sip "10".
- [ ] Pick up the phone on sip "11".

## Mailchimp Integration

- [x] Create a Campaign and Target List for MailChimp.
- [x] Sync Target List with EspoCRM into MailChimp.
- [x] Configure bulk email Campaign into MailChimp.
- [x] Start bulk email Campaign.
- [x] Check recieved emails.

## Real Estate

- [x] Test properties and requests matching.
