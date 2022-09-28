# SMS Sending

In order to send SMS and MMS of any kind to EspoCRM (sending SMS manually, mass SMS, SMS notifications, SMS Two Factor Authentication), you first need to install the [SMS Providers](https://github.com/espocrm/ext-sms-providers/) extension.

The following SMS Providers are currently supported out-of-the-box:

- Twilio
- Spryng
- sms77
- smstools
- SerwerSms 

You can also create your own integration for your SMS Provider using [this example](https://github.com/espocrm/ext-sms-providers/pulls?q=is%3Apr+is%3Aclosed).

In this article:

* [SMS Providers Extension Installation and Configuring](#sms-providers-extension-installation)
* [Manual SMS Sending](#manual-sms-sending)
* [Mass SMS Sending](#mass-sms-sending)
* [Notification SMS Sending](#notification-sms-sending)
* [SMS Two Factor Authentication](#sms-two-factor-authentication)

## SMS Providers Extension Installation and Configuring

In the [espocrm/ext-sms-providers](https://github.com/espocrm/ext-sms-providers/) repository, go to the **Releases** tab and download the `sms-providers-1.4.0.zip` archive (or any other latest version).

After you have downloaded the required archive with the extension, go to your instance in the browser to the *Administration* -> *Extensions* tab and upload the downloaded archive, then install it.

After SMS Providers extension installation, go to *Administration* -> *SMS* and select the **SMS Provider** you need in the drop-down list. Also, in the **SMS From Number** field, enter the number with the country code (*like +11111111111*) from which you will send SMS messages.

### Configuring SMS Providers Extension for Twilio

In order for Twilio Integration to work properly both for receiving / making calls, and for sending / receiving SMS and MMS messages, first configure it according to this instruction in the documentation.


## Manual SMS Sending

## Mass SMS Sending

## Notification SMS Sending

## SMS Two Factor Authentication
