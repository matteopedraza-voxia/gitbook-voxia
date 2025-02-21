---
layout:
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
---

# Bring Your Own Twilio

This document provides a guide on creating a Twilio account, purchasing phone numbers, retrieving your Account SID and Auth Token, and using these credentials in Voxia’s app.

### Create a Twilio Account

1. **Visit the Twilio Website:** Go to [Twilio](https://twilio.com/)
2. **Sign Up:** Click on the “Start for free” button located in the top right corner of the homepage.
3. **Fill Out Registration Form:** Enter your personal details such as your name, email address, and a password.
4. **Verify Your Email:** Check your email inbox for a verification email from Twilio, and click the link provided to verify your account.
5. **Complete Phone Verification:** Twilio will ask for your phone number to send a verification code. Enter this code on the website to complete the verification process.

### Buy a Twilio Phone Number

1. **Log In to Your Account:** After completing registration, log into your Twilio account.
2. **Navigate to the Dashboard:** Go to the dashboard and select “Phone Numbers” from the side menu.
3. **Purchase a Number:** Click on “Buy a Number” to choose your desired phone number. Ensure the number supports voice capabilities to use Voxia's service, and SMS if desired. Note that some countries may require additional verification for messaging services.
4. **Confirm Your Purchase:** Once you select your number, confirm the purchase and complete any required payment information.

{% hint style="info" %}
Twilio official documentation [link](https://help.twilio.com/articles/223183168-Buying-a-toll-free-number-with-Twilio)
{% endhint %}

### Retrieve Your Account SID and Auth Token

1. **Access the Console Dashboard:** Once logged in, your Twilio Console dashboard will display.
2. **Find the SID and Token:** On the dashboard, look for the ‘Account Info’ section. Here you will find your Account SID and Auth Token.

<div align="center" data-full-width="false"><figure><img src="../.gitbook/assets/Twilio auth.png" alt="" width="563"><figcaption></figcaption></figure></div>

{% hint style="info" %}
Twilio official documentation [link](https://help.twilio.com/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-)
{% endhint %}

### Configure Twilio in Voxia's Platform

1. **Log In to Voxia:** Sign into your [Voxia](https://app.voxia.ai/) account.
2. **Navigate to the Integration Tab:** On the left sidebar, click on the “Integrations” tab.
3. **Connect Twilio:** Click on “Connect” next to the Twilio integration.
4. **Enter SID and Auth Token:** Fill in your Twilio Account SID and Auth Token in the fields provided and click on “Connect".
5. **Set Up Your Campaign:** Go to your campaign’s settings in Voxia and select the Twilio numbers you purchased for your campaign. If you don't see your phone numbers, click on "Refresh" to update the list.

{% hint style="info" %}
### Allowing Calls for Specific Countries

To ensure that your campaign can make calls to specific countries, follow these steps:

1. Navigate to the top navigation bar in your Twilio account.
2. Search for 'Voice Geographic Permissions'.
3. In the Voice Geographic Permissions page, you'll see a list of countries.
4. Select the countries that you wish to add to the permissions for your calls.
5. After selecting the desired countries, click on the 'Save' button to apply the changes.

**Note:** Pricing may vary from country to country. You can see the specific rates in the table under the 'PRICE/MINUTE' column.
{% endhint %}
