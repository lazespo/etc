## Role

Create a Role in Espo at Administration > Roles. This Role will be used by the API User. When creating the Role, you need to specify permissions:

* Assignment Permission – specify 'all' if you need the ability to assign records to any user;
* User – set 'Enabled', set Read to 'all' if you need the ability to assign records to any user;
* Lead – set 'Enabled', set Create to 'yes', Read to 'all'; set Edit if you need to update records through Zapier;
* Webhooks – set 'Enabled' if you need records being sent from Espo to Zapier.

## API User

Create an API User in Espo at Administration > API Users. Select the Role that you have created before. The user's API key is available on the user's detail view after creation. You will need to use this API Key when connecting to Zapier.

## Site URL

Obtain the Site URL. It's an URL that you open in the browser to use EspoCRM. You can find it and copy in Espo at Administration > Settings > Site URL.

!!! important

    The Site URL must not contain a trailing slash. If you copied it from the browser's address bar, the slash usually is added. You need to remove it.

!!! note

    To integrate Zapier with EspoCRM instance without a SSL certificate, go to Zapier settings > Advanced > SSL Check and mark the *Disable SSL Certificate Checks* checkbox.

You will need to use the Site URL when connecting to Zapier.

## Usage example

This example will change the lead status after it is created in Espo instance.

1. Press the *Create* button and select the Zaps section to create a new automated workflow.
   
![image](https://github.com/lazespo/etc/assets/99325916/25a8aa5c-7b01-48b6-ad97-88cec584b389)

2. Press the *Trigger* button, enter `espocrm` in the search bar and select EspoCRM (1.0.0) trigger.

![image](https://github.com/lazespo/etc/assets/99325916/dc5b11a5-8412-4b0a-af34-99eaa165c38c)

![image](https://github.com/lazespo/etc/assets/99325916/527f21fd-d8d1-416f-8c49-f9b286b325a6)

3. Select *New Lead* event from the menu on the right in the App & Event section.

![image](https://github.com/lazespo/etc/assets/99325916/366b08de-7080-4436-a737-3457e04cb49d)

4. Press the *Sign In* button in the Account section.

![image](https://github.com/lazespo/etc/assets/99325916/04db5d14-321f-4170-aa5e-91cb25d62e61)

5. In the opened window insert the [Site URL](#site-url) and [API Key](#api-user), then press *Yes, Continue to EspoCRM (1.0.0)* button.

![image](https://github.com/lazespo/etc/assets/99325916/e4d1bef5-686d-4aac-9f0d-4df2066f02a4)

6. Return to the zap creation page and go to the Test tab to test the trigger and press the *Test trigger* button

![image](https://github.com/lazespo/etc/assets/99325916/101061e5-1368-4a33-8808-ed4a59536c35)

7. Select the lead to test (make sure there are already leads in the instance). After that, click the *Continue with selected record* button.

![image](https://github.com/lazespo/etc/assets/99325916/233eb321-48be-422c-a51a-efeb65886192)

8. In the opened window enter `espocrm` in the search bar and select EspoCRM (1.0.0) action.

![image](https://github.com/lazespo/etc/assets/99325916/25d71eab-2ec6-44c3-bfe7-3c482f46ab5d)

9. Select *Update Lead* event from the menu on the right in the App & Event section.

![image](https://github.com/lazespo/etc/assets/99325916/d23b7abc-a075-40f3-ada9-89eb615f6835)

10. Go to Action section and select record ID (ID > Custom > ID).
     
![image](https://github.com/lazespo/etc/assets/99325916/d93b1a66-05cb-474b-90f9-7ce736593c4c)

11. Select the status to which the lead initial status will change after it is created.
    
![image](https://github.com/lazespo/etc/assets/99325916/adb8d8c7-8144-4e86-b7c9-64c42b9d8a2c)

12. Go to Test section and press *Test step* button to make sure that the zap is configured correctly.

![image](https://github.com/lazespo/etc/assets/99325916/d69bfb2d-be2c-422e-bf76-7d4b7a0d4802)

13. Check the lead in your instance, its status should change.

14. Press *Publish* button on the zap creation page.

![image](https://github.com/lazespo/etc/assets/99325916/345a0a9b-6ffa-4415-9404-85cd9b78b4a5)

After successfully publishing this zap, the status of leads created in the instance will change to the one that was selected in the action.
