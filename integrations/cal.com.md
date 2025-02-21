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

# Cal.com

Integrate Cal.com with Voxia to seamlessly schedule meetings. This integration allows you to leverage the power of Cal.com’s scheduling capabilities directly through Voxia’s voice agents, streamlining your scheduling process and improving efficiency.&#x20;

### Connecting Cal.com to Voxia

* **Navigate to the Integrations Tab:** Sign into your Voxia account and go to the "Integrations" tab.
* **Connect Cal.com:** Click on `Connect` next to the Cal.com integration. A new window will open where you need to enter your API Key from Cal.com to authorize Voxia to access your account.

<figure><img src="../.gitbook/assets/Untitled design.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**If you do not have an API Key, follow these steps to create one:**

1. Log in to Cal.com and navigate to Settings located at the bottom left of the dashboard.
2. In the side menu, find and click on "API keys" under the Developer section.
3. Press the `Add` button to create a new API key. A new window will appear where you need to name your API key. **Make sure to enable the "Never expires" toggle** to ensure your API key does not expire.
4. Click `Save` to generate the API key. Make sure to copy this API key immediately; once you click `Done`, you will not be able to view or retrieve it again. If you lose your API key, you will need to repeat the process and create a new one.

Use the copied API key to complete the connection process in your Voxia account by pasting it into the required field.
{% endhint %}

### Adding a Cal.com Step in a Campaign

{% hint style="warning" %}
Note that to add this step, you need to have an **`Email`** for each contact.
{% endhint %}

* Press the `Schedule a Meeting` button.
* Before offering time slots from your account, decide on the content for the assistant to say.
* Choose the relevant event from the dropdown.
* Define how many days in advance clients can schedule meetings by setting the 'Schedule days ahead' field.
* For scenarios when no time slots are available, configure how the assistant should react:
  * **Avoid Calling**: Select this option to prevent the assistant from making calls when no slots are available.
  * **Use Fallback Phrase**: Choose this option to have the assistant use a fallback phrase. Upon selection, a text field will open where you can insert the specific sentence the assistant should say.

<figure><img src="../.gitbook/assets/Screenshot 2024-08-16 at 19.23.14.png" alt=""><figcaption></figcaption></figure>

### Verifying Cal.com Settings <a href="#verifying-calendly-settings" id="verifying-calendly-settings"></a>

To ensure seamless integration between Voxia and Cal.com, verify the event settings within Cal.com:

1. Log in to your Cal.com account and navigate to the event you wish to integrate with Voxia.
2. Go to the _**Advanced**_ tab within the event settings.
3. Any additional questions must be marked as **optional**. Events with required additional questions cannot be used in Voxia.

<div align="center"><figure><img src="../.gitbook/assets/Screenshot 2024-08-16 at 20.36.15.png" alt=""><figcaption></figcaption></figure></div>

### Adding Contact's Phone Number to the Invite

* **Access Event Settings:** Navigate to your Cal.com account and select the event integrated with Voxia and go to the _**Advanced**_ tab within the event settings.
* **Add a New Question:** Scroll to the **Booking questions** section and click on the `Add a question` button.
* **Configure the Question Settings:**
  * Set the **Input type** to 'Short Text'.
  * For the **Identifier**, enter 'phone'.
  * Ensure the **Disable input if the URL identifier is prefilled** option is unchecked.
  * Set **Required** to 'No'.
* **Customization Options: Label** and **Placeholder** are the only fields you are free to customize. Adjust these as necessary to fit the context of your event.
* **Save the Configuration:**
  * Click `Add` to include the field in your invite.
  * Ensure to click `Save` at the top right of the event settings to apply your changes.

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>
