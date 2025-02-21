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

# Cal.com Integration

Integrate Cal.com with Voxia to seamlessly schedule meetings. This integration allows you to leverage the power of Cal.com’s scheduling capabilities directly through Voxia’s voice agents, streamlining your scheduling process and improving efficiency.&#x20;

### Connecting Cal.com to Voxia

* **Navigate to the Integrations Tab:** Sign into your Voxia account and go to the "Integrations" tab.
* **Connect Cal.com:** Click on `Connect` next to the Cal.com integration. A new window will open prompting you to enter your **API Key** from Cal.com to authorize Voxia.

<figure><img src="../.gitbook/assets/Untitled design.png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**If you do not have an API Key, follow these steps to create one:**

1. Log in to **Cal.com** and navigate to **Settings** (located at the bottom left of the dashboard).
2. In the side menu, find and click on **"API keys"** under the **Developer** section.
3. Click `Add` to create a new API key.&#x20;
4. Name your API key, And enable the **"Never expires"** toggle to prevent expiration.
5. Click `Save` to generate the API key.&#x20;
6. Copy the API key, as it will not be retrievable once you click **Done**.
7. Paste the copied API key into Voxia to complete the connection.
{% endhint %}

### Adding a Cal.com Step in a Voxia Campaign

{% hint style="warning" %}
Note that to add this step, each contact must have an **`Email`**.
{% endhint %}

* Press the `Schedule a Meeting` button.
* Determine the **assistant's spoken content** before offering time slots.
* Choose the relevant **event** from the dropdown.
* Set how many days in advance clients can schedule meetings by setting the **'Schedule days ahead'** field.

### Handling No Available Time Slots

* **Avoid Calling**: Prevents the assistant from making calls when no slots are available.
* **Use Fallback Phrase**: Allows the assistant to use a custom fallback phrase.
  * Enter the phrase in the provided text field.

<figure><img src="../.gitbook/assets/Screenshot 2024-08-16 at 19.23.14.png" alt=""><figcaption></figcaption></figure>

### Verifying Cal.com Settings <a href="#verifying-calendly-settings" id="verifying-calendly-settings"></a>

To ensure seamless integration with Voxia, verify the event settings within Cal.com:

1. Log in to your **Cal.com**&#x20;
2. Navigate to the event you want to integrate with Voxia.
3. Open the **Advanced** tab within the event settings.
4. Ensure **additional questions are optional** (events with required questions cannot be used in Voxia).

<div align="center"><figure><img src="../.gitbook/assets/Screenshot 2024-08-16 at 20.36.15.png" alt=""><figcaption></figcaption></figure></div>

### Adding Contact's Phone Number to the Invite

* **Access Event Settings:** Navigate to your Cal.com account and select the event integrated with Voxia and go to the _**Advanced**_ tab within the event settings.
* **Add a New Question:** Scroll to the **Booking questions** and click `Add a question`.
* **Configure the Question Settings:**
  * Set the **Input type** to 'Short Text'.
  * For the **Identifier**, enter 'phone'.
  * Ensure the **Disable input if the URL identifier is prefilled** option is unchecked.
  * Set **Required** to 'No'.
* **Customization Options:** Only **Label** and **Placeholder** fields are customizable. Adjust these as necessary to fit the context of your event.
* **Save the Configuration:**
  * Click `Add` to include the field in your invite.
  * Click `Save` at the top right of the event settings to apply changes.

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>
