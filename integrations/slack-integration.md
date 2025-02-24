# Slack Integration

Enhance your Voxia experience by integrating it with Slack to receive call details directly in your chosen channels. This integration allows you to effortlessly access summaries and key insights from selected call groups, keeping your team informed and connected.

### Connecting to your Slack organization

* **Navigate to the Integrations Tab:** Sign into your Voxia account and go to the "Integrations" tab.
* **Connect Slack:** Click on `Connect` under the Slack logo. A new window will open where you need to select the Slack channel to authorize Voxia to publish the calls details.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-21 at 13.21.34.png" alt=""><figcaption><p>Press the Connect button.</p></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-02-21 at 12.58.05.png" alt=""><figcaption><p>Authorize Voxia, and select the channel where details will be published.</p></figcaption></figure>

{% hint style="info" %}
If you don't have any channel to select, go to Slack and create a new channels for Voxia notifications.\
To create a new channel, follow the instructions [here](https://slack.com/help/articles/201402297-Create-a-channel).
{% endhint %}

Once you allow the connection, you will notice that the Slack feature is shown as "Connected".

### Setting your Campaign with the integration

* Go to the desired campaign.
* Click on "Edit" to enter the Setup section.
* At the bottom of the Setup section, you will find the Slack integration configuration as Connected.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-21 at 15.24.29.png" alt=""><figcaption></figcaption></figure>

* To customize which calls trigger a Slack notification, click on the **Call Notification** dropdown and select the specific call types you wish to receive notifications for.

<figure><img src="../.gitbook/assets/Screenshot 2025-02-21 at 15.23.44.png" alt=""><figcaption></figcaption></figure>

### Slack notification from Voxia

Once the call has ended, a Slack message will appear in the selected channel.

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption><p>Voxia Slack notification example.</p></figcaption></figure>

This message can be divided into sections.

1. **Call information**
   * You can check the call analysis outcome and total call time.
2. **Campaign name**
3. **Contact information**
4. **Summary**
   * Every Key Question added to the summary, matching the information you find in Voxia.
5. **Other information**
   * Any other information depending on the Campaign set up, like SMS sending.
6. **Link to the call details in Voxia.**

<figure><img src="../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
As the connection is created through your organization, you can choose one or more Campaigns to trigger the Slack notifications.
{% endhint %}

