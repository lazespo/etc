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
- [ ] Apply for imported emails (Group Email).

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

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

### Target List

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Populate the target list with leads using 'select all results'.

### Calendar

- [ ] Create events.
- [ ] A shared view.
- [ ] Timeline.

### Meeting

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Send invitations.
- [ ] Popup reminder.
- [ ] Email reminder.

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

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

### Knowledge Base

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Send in email.

### Document

- [x] Creating.
- [x] Updating.
- [x] Removing from List View.
- [x] Removing from Detail View.
- [x] Duplicating.
- [x] Creating by drag-n-drpping file on the list view.

### User

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

### Team

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Assign a team position to a user (Position List field).

### PDF Template

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

## Features

### Personal Email Account

- [x] Create account with IMAP and SMTP.
- [x] Check emails are received and available in the user's INBOX.
- [x] Test email sending from the account.

### Group Email Account

- [ ] Create account with IMAP and SMTP.
- [ ] Check emails are received.
- [ ] Test email sending from the account.
- [ ] Email-to-Case.

### Email

- [ ] Apply email template, test placeholders.
- [ ] Save draft and send.
- [ ] Remove email.

### Stream

- [ ] Post on record.
- [ ] Post attachments.
- [ ] Update post.
- [ ] Remove post.
- [ ] Post to another user.
- [ ] Post to team.

### Portal

- [ ] Create a portal, with portal role, portal user, layout set.
- [ ] Check whether ACL is applied for the portal user.
- [ ] Check whether layout set is applied for a logged portal user.

### 2-factor authentication

- [ ] Set up TOTP 2FA for a user and login under that user.

### Passwords

- [ ] An admin creates a user (with an email address non-empty), password is empty, *Send Email with Access Info to User* is checked. Check a received access email. Try to login under the new user.
- [ ] An admin changes a password to another user (on the User edit view). 
- [ ] An admin changes a password to another user with *Send Email with Access Info to User* checked (the user should have email address). Check a received email.
- [ ] A regular user changes own password (from the dropdown on the User detail view).
- [ ] Send password change link for another regular user (under the admin from the dropdown on the User detail view).
- [ ] Send password change link for a portal user.
- [ ] Forgot password from the login page. Recover access for a user.

### Import

- [ ] Import CSV with email address, phone number.
- [ ] Import Create Only.
- [ ] Import Create and Update.
- [ ] Check duplicate detection.
- [ ] Import invalid email, check the record is available in the Errors panel.
- [ ] Import in idle.
- [ ] Import by command line (manully).
- [ ] Import with same params.
- [ ] Revert import.

### Currency

- [ ] Currency converting.

### Entity Manager

- [ ] Create a custom entity.
- [ ] Edit entity.
- [ ] Edit formula.
- [ ] Create custom field.
- [ ] Edit custom field.
- [ ] Delete custom field.
- [ ] Delete custom entity.

### Layout sets

- [ ] Create a layout set.
- [ ] Apply the layout set to a team and test it's working for a logged user (the team should be a default team for the user).

### Lead Capture

- [ ] Set up lead capture without opt-in confirmation, send API request, check lead is created.
- [ ] Set up lead capture with opt-in confirmation, send API request, check whether works properly.
- [ ] Check duplicate detecting works properly.

### Mass Email

- [ ] Send mass email.
- [ ] Tracking URL in mass email.

## OIDC

- [ ] Create User.
- [ ] Change Username Claim.
- [ ] Allow OIDC login for admin users.
- [ ] Sync Teams.

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
- [ ] Grid type report with non-aggregate fields (non-grouping).
- [ ] Grid type report with non-aggregate fields (grouping).
- [ ] Report dashlet Grid.
- [ ] Report dashlet List.
- [ ] Report Panel.
- [ ] Report Filter.
- [ ] Send report in Email (from UI).
- [ ] Print to PDF.

### Workflow

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating. 
- [ ] Action "Send Email".

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
- [ ] Printing to PDF.
- [ ] Sending PDF in email.

### Invoice

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.
- [ ] Printing to PDF.
- [ ] Sending PDF in email.

### Product

- [ ] Creating.
- [ ] Updating.
- [ ] Removing from List View.
- [ ] Removing from Detail View.
- [ ] Duplicating.

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

- [ ] Create a Campaign and Target List for MailChimp.
- [ ] Sync Target List with EspoCRM into MailChimp.
- [ ] Configure bulk email Campaign into MailChimp.
- [ ] Start bulk email Campaign.
- [ ] Check recieved emails.

## Real Estate

- [ ] Test properties and requests matching.
