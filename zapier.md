## Role

Create a Role in Espo at Administration > Roles. This Role will be used by the API User. When creating the Role, you need to specify permissions:

* Assignment Permission – specify 'all' if you need the ability to assign records to any user;
* Lead – set 'Enabled', set Create to 'yes', Read to 'all'; set Edit if you need to update records through Zapier;
* Webhooks – set 'Enabled' if you need records being sent from Espo to Zapier.

## Api User

Create an API User in Espo at Administration > API Users. Select the Role that you have created before. The user's API key is available on the user's detail view after creation. You will need to use this API Key when connecting to Zapier.

## Site URL

Obtain the Site URL. It's an URL that you open in the browser to use EspoCRM. You can find it and copy in Espo at Administration > Settings > Site URL.

!!! important

The Site URL must not contain a trailing slash. If you copied it from the browser's address bar, the slash usually is added. You need to remove it.

You will need to use the Site URL when connecting to Zapier.

## Usage example

1. Press the Create button and select the Zaps section to create a new automated workflow.
![image](https://github.com/lazespo/etc/assets/99325916/25a8aa5c-7b01-48b6-ad97-88cec584b389)
2. Press the Trigger button, enter EspoCRM in the search and select EspoCRM (1.0.0) trigger.
![image](https://github.com/lazespo/etc/assets/99325916/dc5b11a5-8412-4b0a-af34-99eaa165c38c)
![image](https://github.com/lazespo/etc/assets/99325916/527f21fd-d8d1-416f-8c49-f9b286b325a6)
3. Select New Lead event from the menu on the right.
![image](https://github.com/lazespo/etc/assets/99325916/366b08de-7080-4436-a737-3457e04cb49d)
4. 
