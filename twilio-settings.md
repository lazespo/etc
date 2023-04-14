1. Create Twilio Account: https://www.twilio.com/try-twilio.
![Screenshot from 2023-04-14 14-27-50](https://user-images.githubusercontent.com/99325916/232032089-120cdfa0-147a-4265-8240-962591763571.png)
2. In the list on the left, go to United States (US1) (or any other country) > Phone Numbers > Manage > Active Numbers and buy a number by pressing *Buy a number* button in the upper-right corner.
![2](https://user-images.githubusercontent.com/99325916/232032162-c23f0f83-b892-40fc-8e6f-8278f8785f62.png)
3. Select the number that suits you and press the *Buy* button.
![Screenshot from 2023-04-14 13-27-12](https://user-images.githubusercontent.com/99325916/232032345-aaf9b5a2-4907-4201-af5a-63b605c2d555.png)
4. Search for the `sip` word and go to *Voice SIP Domains*, then press the **plus** button to create SIP Domain.
![Screenshot from 2023-04-14 13-29-14](https://user-images.githubusercontent.com/99325916/232032421-dba685de-5295-4e9b-92e2-8802f62c2335.png)
5. Fill up Friendly Name for your SIP Domain, its SIP URL, then create a Credential List by pressing **plus** button in *Voice Authentication* section. In the *SIP Registration* section, click on the Disable slider to enable it, and select the Credential List you created. SIP URL and SIP Credentials usernames will be used in the following points to connect the user to the SIP client and more.
![Screenshot from 2023-04-14 13-31-47](https://user-images.githubusercontent.com/99325916/232032489-be8e110b-7c9b-43e3-af40-3d3091b860d7.png)
![Screenshot from 2023-04-14 13-57-42](https://user-images.githubusercontent.com/99325916/232032525-857adc11-23dc-447d-a7ba-9355a171b344.png)
6. Go to your instance of EspoCRM, click on the three dots in the top right corner and select your User. Paste the following value into Phone field in the following format: `credential_username@SIP_URL.sip.twilio.com`. It should look something like this (it is important that the Phone type is SIP, as in the screenshot):
![image](https://user-images.githubusercontent.com/99325916/232032890-e2df18b2-22a7-46b0-a060-efacfbbaca1c.png)
7. In your EspoCRM instance, go to Administration > Integrations > VoIP » Twilio and configure everything as follows: https://docs.espocrm.com/extensions/voip-integration/twilio-integration-setup/#how-to-configure-twilio-integration-for-an-administrator.
8. Click *Test Connection* button and save the Connector.
9. Go to United States (US1) (or any other country) > Phone Numbers > Manage > Active Numbers > the number you purchased and in the *Voice and Fax* and *Messaging* sections, set the following settings:
![Screenshot from 2023-04-14 13-51-00](https://user-images.githubusercontent.com/99325916/232032973-01fe7cca-d892-4f7d-b9a8-2683459cc168.png)
![Screenshot from 2023-04-14 13-51-05](https://user-images.githubusercontent.com/99325916/232032994-a1aa6ff4-0e82-43d8-bdc4-7a219ea03d02.png)
10. Go to your EspoCRM instance and configure VoIP Router as indicated in the following instructions: https://docs.espocrm.com/extensions/voip-integration/twilio-integration-setup/#how-to-configure-routing-of-twilio-phone-numbers.
11. Log in to any convenient SIP client (for example, Zoiper) using the credentials created in step 5, where the username will is in the `credential_username@SIP_URL.sip.twilio.com` format, the password is the one you specified for this credential.
![Screenshot from 2023-04-14 14-37-21](https://user-images.githubusercontent.com/99325916/232033868-26d9c6e3-214d-43b1-9b79-e12d0a13728f.png)
![Screenshot from 2023-04-14 14-37-26](https://user-images.githubusercontent.com/99325916/232033885-d382e8ac-c951-4e18-965c-13d9c173a2b7.png)
![Screenshot from 2023-04-14 14-37-33](https://user-images.githubusercontent.com/99325916/232033910-9fb6076b-93e8-41e0-8417-3fd7a9d27a92.png)
![Screenshot from 2023-04-14 14-37-51](https://user-images.githubusercontent.com/99325916/232033936-afcc4f23-8547-46b4-b05c-d095295fa47a.png)
![Screenshot from 2023-04-14 14-37-59](https://user-images.githubusercontent.com/99325916/232033979-fea7b971-b426-45c2-9168-8a0540623182.png)
![Screenshot from 2023-04-14 14-38-08](https://user-images.githubusercontent.com/99325916/232033997-0eb5a568-db38-4002-b794-427ed1ef140b.png)
12. Make a call from your EspoCRM instance by clicking on the phone number, accept the call in the SIP client and wait for the call to reach the desired number.

Note: If the call drops, check Twilio's *Voice Geographic Permissions*: https://console.twilio.com/us1/develop/voice/settings/geo-permissions. Mark your country with a checkbox and click on the *Save* button.
![Screenshot from 2023-04-14 14-05-46](https://user-images.githubusercontent.com/99325916/232033355-86a50653-a540-4ae8-9137-ecb55abce626.png)
