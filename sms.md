# SMS Sending

In order to send SMS and MMS of any kind to EspoCRM (sending SMS manually, mass SMS, SMS notifications, SMS Two Factor Authentication), you first need to install the [SMS Providers](https://github.com/espocrm/ext-sms-providers/) extension.

The following SMS Providers are currently supported out-of-the-box:

- [Twilio](#configuring-sms-providers-extension-for-twilio)
- Spryng
- sms77
- smstools
- SerwerSms 

You can also create your own integration for your SMS Provider using [this example](https://github.com/espocrm/ext-sms-providers/pulls?q=is%3Apr+is%3Aclosed).

### Configuring SMS Providers Extension for Twilio

In order for Twilio Integration to work properly both for receiving / making calls, and for sending / receiving SMS and MMS messages, first configure it according to [this instruction](https://docs.espocrm.com/extensions/voip-integration/twilio-integration-setup/). Be sure to check the functionality of [VoIP Extension](https://www.espocrm.com/extensions/voip-integration/) for Twilio Integration. After that, you can proceed to the full installation and configuration of the SMS Providers extension.

---

In this article:

* [SMS Providers Extension Installation and Configuration](#sms-providers-extension-installation-and-configuration)
* [Manual SMS Sending](#manual-sms-sending)
* [Mass SMS Sending](#mass-sms-sending)
* [Notification SMS Sending](#notification-sms-sending)
* [SMS Two Factor Authentication](#sms-two-factor-authentication)

## SMS Providers Extension Installation and Configuration

In the [espocrm/ext-sms-providers](https://github.com/espocrm/ext-sms-providers/) repository, go to the **Releases** tab and download the `sms-providers-1.4.0.zip` archive (or any other latest version).

After you have downloaded the required archive with the extension, go to your instance in the browser to the *Administration* -> *Extensions* tab and upload the downloaded archive, then install it.

After SMS Providers extension installation, go to *Administration* -> *SMS* and select the **SMS Provider** you need in the drop-down list. Also, in the **SMS From Number** field, enter the number with the country code (*like +11111111111*) from which you will send SMS messages.

Next, go to *Administration* -> *Integrations* and set up the SMS Provider you need.


## Manual SMS Sending

## Mass SMS Sending

To send mass SMS, you will need to create a Report and Workflow ([Advanced Pack](https://www.espocrm.com/extensions/advanced-pack/) extension features).

To begin with, you need to create a Report with a list of contacts/leads/accounts for which you want to send SMS. You can learn more about Reports [here](https://docs.espocrm.com/user-guide/reports/).

After that, you need to create a Workflow with the *Target Entity* for which you created the Report (Contact/Lead/Account), and with the *Trigger Type* **[Scheduled](https://docs.espocrm.com/administration/workflows/#scheduled)**. Set Scheduling as you need, with what frequency SMS should be sent. You can learn more about Workflows [here](https://docs.espocrm.com/administration/workflows/).

After that, for this Workflow, select **Execute Formula Script** *Action* and paste this formula:

```
$body = string\concatenate('Hi, ', name, '! This is SMS notification from EspoCRM.');

$smsId = record\create(
    'Sms',
    'to', phoneNumber,
    'body', $body
);

ext\sms\send($smsId);
```

This action uses the creation of a variable (*$body*) using **[string\concatenate](https://docs.espocrm.com/administration/formula/#stringconcatenate)** formula, which stores the plain text and the attribute of the entity (*name*). You can paste any other text. This will be the **body** of your SMS.


## Notification SMS Sending

To send SMS notification, you will need to create a Workflow ([Advanced Pack](https://www.espocrm.com/extensions/advanced-pack/) extension feature). 
You can learn more about Workflows [here](https://docs.espocrm.com/administration/workflows/).

You can choose any *Target Entity* and *Trigger Type* you want. In any case, at the end you will need to select **Execute Formula Script** *Action* and paste this formula:

```
$body = 'Hi! This is SMS notification from EspoCRM.';

$smsId = record\create(
    'Sms',
    'to', '+11111111111',
    'body', $body
);

ext\sms\send($smsId);
```

This action uses the creation of a variable (*$body*) , which stores the plain text. You can paste any other text. This will be the **body** of your SMS.

## SMS Two Factor Authentication
