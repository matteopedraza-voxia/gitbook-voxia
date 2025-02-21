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

# Campaign Setup

The Campaign Setup allows you to configure essential details for your campaign, including the campaign name, company information, phone numbers, and various settings. Proper setup ensures that your campaign runs smoothly and effectively aligns with your business goals.

## **Setting Up a Campaign**

* **Name Your Campaign**: In the window that appears, enter a name for your campaign.
* **Select Campaign Type**: Choose whether the campaign is `Outgoing` or `Incoming`.
* **Toggle Recording**: Activate this option if you wish to record calls.
* **Toggle Do Not Call Registry**: Activate this option to prevent calls to numbers listed on the US Federal Do Not Call registry.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

### **Selecting Phone Numbers**

{% hint style="info" %}
**If your Twilio account is not connected, follow these steps:**

1. If your Twilio account is not connected, click the `Connect Twilio` button.
2. Enter your Twilio Account SID Token and Auth Token.
3. Phone numbers should appear in the list. If not visible, click the `Refresh` button.
{% endhint %}

#### **Outgoing Campaigns**:

Select phone numbers from your connected Twilio account. Each call attempt will rotate through the chosen numbers in sequence until all are used, and then the cycle restarts from the first number.

#### **Incoming Campaigns**:

Choose a phone number for contacts to call into.

### **Voice Selection**

* **Choose a Voice**: Select a voice from the provided list for your campaign.
* **Test Voice**: Click the play icon next to the sample text to hear the voice. You may enter a preferred sentence for testing.

{% hint style="info" %}
**Clone a Voice:** If you are interested in cloning a voice, please speak with your account manager to discuss the process.
{% endhint %}

<figure><img src="../.gitbook/assets/image (35).png" alt="" width="563"><figcaption></figcaption></figure>

### **Availability Settings**

#### **Outgoing Campaigns**

* **Time Zone**: Select your preferred time zone for making calls.
* **Calling Days and Hours**: Choose your preferred days and the time window for calling.
* **Dial Attempts**:
  * **Maximum Daily Attempts**: Set the maximum number of calls to be made to a contact per day.
  * **Total Dial Attempts**: Specify the total number of attempts before stopping. The system will continue calling until this limit is reached.
* **Wait Time Between Attempts**: Choose the minimum wait time between attempts, with options to switch between hours and minutes.

#### **Incoming Campaigns**

* **Time Zone**: Only the time zone selection is required, specifically useful for scheduling meetings.

<figure><img src="../.gitbook/assets/image (36).png" alt="" width="563"><figcaption></figcaption></figure>

### **Setup Webhook**

Enter the Webhook URL at the bottom to send call details to other apps post-call.

{% hint style="info" %}
See the [API documentation](../webhook/webhook-overview.md) on Webhook for more details.
{% endhint %}

## **Saving Your Campaign**

Click on `Save changes` located at the top right of the window to finalize your campaign settings. After saving, you will see the new campaign appear in your dashboard.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

{% hint style="success" %}
Once you have configured your campaign, you are ready to launch.&#x20;

For **outgoing campaigns**, upload your contacts directly through the [app](../using-voxia/uploading-contacts.md) or by using our [API](../api/add-contacts.md).
{% endhint %}
